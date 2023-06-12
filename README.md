Public Class Form1
    Private Sub cmdBoton_Click(sender As Object, e As EventArgs) Handles cmdBoton.Click
        Dim Numero As Integer
        Dim Valor1 As Integer
        Dim Valor2 As Integer
        Numero = txtNum.Text
        Do
            Valor1 = 0
            Do
                Valor2 = Numero
                Numero = Numero \ 10
                Valor2 = Valor2 Mod 10
                Valor1 = Valor1 + Valor2
            Loop Until Numero = 0
            Numero = Valor1 \ 10
            If Numero <> 0 Then
                Numero = Valor1
            End If
        Loop Until Numero = 0
        lblUnidadMinima.Text = "La Unidad Minima Es " & Valor1
    End Sub
End Class
