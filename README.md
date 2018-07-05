<html>
<head >
    <title>Conta Corrente</title>
    <link rel ="stylesheet" type="text/js" href="opa.js"/>
    <link rel ="stylesheet" type="text/css " href="opa.css"/>
</head>
<body>
<form name="form1" method="post" action="">
    <p>
    Deposito <br>
    <input type="text" name="deposito">
    </p>
    <p>
    Valor <br>
    <input type="text" name="valor"><br>
    <input type="submit" value="Credito" name="botao">
    <input type="submit" value="Debito" name="botao">
    </p>
</form>

<h4>Conta Corrente</h4>

<br>

<?php
    if (isset($_POST['botao'])) {
        $botao = $_POST['botao'];
        $deposito = $_POST['deposito'];
        $valor = $_POST['valor'];

        echo "Valor do deposito: $deposito <br>";
        echo "Valor da compra: $valor <br>";

        echo "<br>";

        echo "Seu saldo é de: $deposito R$<br>";
    }
    if (isset($_POST['botao'])) {
        if ($botao == "Debito") {
            $menos = $deposito - $valor;
            echo "Seu saldo apos a compra é de: $menos R$<br>";
        }if ($botao == "Credito") {
            $divisao = $valor / 2;
            $compra = $deposito - $divisao;
            echo "Seu saldo apos a compra é de $compra R$<br>";
        }
    }
?>

</body>
</html>
