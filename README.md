# CLIMA
      
				
<div id="app"></div>

    <!-- Parâmetro sensor é utilizado somente em dispositivos com GPS -->
    <script src="http://maps.google.com/maps/api/js?sensor=false"></script>
    <script type="text/javascript">
      function CalculaDistancia() {
        $('#litResultado').html('Aguarde...');
        // Instancia o DistanceMatrixService.
        var service = new google.maps.DistanceMatrixService();
        // Executa o DistanceMatrixService.
        service.getDistanceMatrix({
            origins: [$("#txtOrigem").val()], // Origem
            destinations: [$("#txtDestino").val()], // Destino
            travelMode: google.maps.TravelMode.DRIVING, // Modo (DRIVING | WALKING | BICYCLING)
            unitSystem: google.maps.UnitSystem.METRIC // Sistema de medida (METRIC | IMPERIAL)
        }, callback); // Vai chamar o callback
      }

      // Tratar o retorno do DistanceMatrixService
      function callback(response, status) {
        // Verificar o status.
        if (status != google.maps.DistanceMatrixStatus.OK) { // Se o status não for "OK".
            $("#litResultado").html(status);
        } else { // Se o status for "OK".
            $("#litResultado").html("&nbsp;"); // Remove o "aguarde".

            // Popula os campos.
            $("#txtOrigemResultado").val(response.originAddresses);
            $("#txtDestinoResultado").val(response.destinationAddresses);
            $("#txtDistancia").val(response.rows[0].elements[0].distance.text);
            var tempo = response.rows[0].elements[0].duration.text;
            tempo = tempo.replace("day", "dia").replace("hour", "hora").replace("min", "minuto");
            $("#txtTempo").val(tempo);

            //Atualizar o mapa.
            $("#map").attr("src", "https://maps.google.com/maps?saddr=" + response.originAddresses + "&daddr=" + response.destinationAddresses + "&output=embed");
        }
      }
    </script>

    <form action="http://www.example.com/url" method="post">
      <div><span>Pesquisa:</span></div>
      <label for="txtOrigem"><strong>Endere&ccedil;o de origem</strong></label>
      <input name="pesquisaOrigem" type="text" id="txtOrigem" class="field" style="width: 400px" value="S&atilde;o Paulo" />
      <label for="txtDestino"><strong>Endere&ccedil;o de destino</strong></label>
      <input name="pesquisaDestino" type="text" id="txtDestino" class="field" style="width: 400px" value="Rio de Janeiro" />
      <input type="button" value="Calcular dist&acirc;ncia" onclick="CalculaDistancia()" class="btnNew" />
      <div><span id="litResultado">&nbsp;</span></div>

      <div><span>Resposta:</span></div>
      <label for="txtOrigemResultado"><strong>Endere&ccedil;o de origem</strong></label>
      <input name="resultadoOrigem" readonly="readonly" type="text" id="txtOrigemResultado" class="field" style="width: 400px" value="" />
      <label for="txtDestinoResultado"><strong>Endere&ccedil;o de destino</strong></label>
      <input name="resultadoDestino" readonly="readonly" type="text" id="txtDestinoResultado" class="field" style="width: 400px" value="" />
      <br />
      <label for="txtDistancia"><strong>Dist&acirc;ncia</strong></label>
      <input name="distancia" readonly="readonly" type="text" id="txtDistancia" value="" /> 
      <label for="txtTempo"><strong>Tempo</strong></label>
      <input name="tempo" readonly="readonly" type="text" id="txtTempo" value="" />
      <input type="submit" value="Enviar para o servidor" />
    </form>

    <div style="padding: 10px 0 0; clear: both">
      <iframe width="750" scrolling="no" height="350" frameborder="0" id="map" marginheight="0" marginwidth="0" src="https://maps.google.com/maps?saddr=S&atilde;o Paulo&daddr=Rio de Janeiro&output=embed"></iframe>
    </div>
  </head>
</html>
