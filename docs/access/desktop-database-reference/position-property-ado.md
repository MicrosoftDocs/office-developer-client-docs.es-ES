---
<<<<<<< Título HEAD: posición (propiedad) (ADO) TOCTitle: posición (propiedad) (ADO) === título: posición (propiedad, ADO) TOCTitle: posición (propiedad, ADO)
>>>>>>> Master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: ms.date 48546709: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="position-property-ado"></a>Position (propiedad, ADO)
=======
# <a name="position-property-ado"></a>Posición (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica la posición actual dentro de un objeto [Stream](stream-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long** que especifica el desplazamiento, en número de bytes, de la posición actual desde el principio de la secuencia. El valor predeterminado es 0, que representa el primer byte de la secuencia.

## <a name="remarks"></a>Comentarios

La posición actual puede moverse a un punto situado detrás del final de la secuencia. Si se especifica la posición actual detrás del fin de la secuencia, el [tamaño](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** aumentará en consecuencia. Cualquier byte nuevo agregado de esta forma será nulo.


> [!NOTE]
> <P>[!NOTA] <STRONG>Position</STRONG> siempre mide bytes. En las secuencias de texto que usan juegos de caracteres multibyte, multiplique la posición por el tamaño de los caracteres para determinar el número de caracteres. Por ejemplo, en un juego de caracteres de dos bytes, el primer carácter se encuentra en la posición 0, el segundo en la 2, el tercero en la 4 y así sucesivamente.</P>



No es posible utilizar valores negativos para cambiar la posición actual en un objeto **Stream**. Con **Position** sólo se pueden utilizar números positivos.

En los objetos **Stream** de sólo lectura, ADO no devolverá un error si **Position** se establece en un valor superior al **tamaño** de **Stream**. Eso no modifica el tamaño de **Stream** ni altera el contenido de **Stream** de ninguna forma. Sin embargo, debe evitarse, ya que da lugar a un valor de **Position** sin sentido.

