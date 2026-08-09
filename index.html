<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Generador de Lista de Jugadores PGN</title>
    <style>
        body { font-family: sans-serif; max-width: 900px; margin: 20px auto; padding: 20px; line-height: 1.6; }
        textarea { width: 100%; height: 250px; font-family: monospace; padding: 10px; margin-bottom: 10px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box; }
        .btn { background-color: #2c3e50; color: white; padding: 10px 20px; border: none; cursor: pointer; border-radius: 4px; font-size: 16px; }
        .btn:hover { background-color: #34495e; }
        .result-container { margin-top: 20px; }
        h2 { color: #2c3e50; }
        .copy-hint { font-size: 0.8em; color: #666; margin-bottom: 5px; }
    </style>
</head>
<body>

    <h2>Generador de Sustitucion de Nombres para transmitir en lichess con CHESSCAM</h2>
    <p>Pega el texto PGN a continuación para extraer la lista de jugadores ordenados por número de tablero.</p>

    <form method="post">
        <textarea name="pgn_input" placeholder="Pega aquí el contenido PGN..."><?php 
            echo isset($_POST['pgn_input']) ? htmlspecialchars($_POST['pgn_input']) : ''; 
        ?></textarea>
        <br>
        <button type="submit" class="btn">Generar Lista</button>
    </form>

    <?php
    if ($_SERVER['REQUEST_METHOD'] === 'POST' && !empty(trim($_POST['pgn_input']))) {
        $input = $_POST['pgn_input'];

        // Dividimos el PGN en bloques de partidas individuales
        $games = preg_split('/\n\s*\n/', $input);
        
        $outputLines = [];
        $boardNumber = 1;

        foreach ($games as $game) {
            $white = '';
            $black = '';

            // Extraemos la etiqueta White
            if (preg_match('/\[White\s+"([^"]+)"\]/', $game, $matchesWhite)) {
                $white = trim($matchesWhite[1]);
            }

            // Extraemos la etiqueta Black
            if (preg_match('/\[Black\s+"([^"]+)"\]/', $game, $matchesBlack)) {
                $black = trim($matchesBlack[1]);
            }

            // Si encontramos al menos un jugador en la partida, agregamos las líneas
            if ($white !== '' || $black !== '') {
                $outputLines[] = "White {$boardNumber}  / / / / " . $white;
                $outputLines[] = "Black {$boardNumber}  / / / / " . $black;
                $boardNumber++;
            }
        }

        $resultText = implode("\n", $outputLines);

        if (!empty($resultText)) {
            echo "<div class='result-container'>";
            echo "<h3>Lista Generada:</h3>";
            echo "<div class='copy-hint'>Haz clic en el área de texto para seleccionar y copiar todo:</div>";
            echo "<textarea readonly onclick='this.select()'>" . htmlspecialchars($resultText) . "</textarea>";
            echo "</div>";
        } else {
            echo "<p style='color: red; margin-top: 15px;'>No se encontraron etiquetas de White o Black válidas en el PGN ingresado.</p>";
        }
    }
    ?>

</body>
</html>
