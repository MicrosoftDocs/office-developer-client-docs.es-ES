---
<<<<<<< Título HEAD: LineSeparator (propiedad) (ADO) TOCTitle: LineSeparator (propiedad) (ADO) === título: LineSeparator (propiedad, ADO) TOCTitle: LineSeparator (propiedad, ADO)
>>>>>>> Master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: ms.date 48546676: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="lineseparator-property-ado"></a>LineSeparator (propiedad, ADO)
=======
# <a name="lineseparator-property-ado"></a>LineSeparator (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**. El valor predeterminado es **adCRLF**.

## <a name="remarks"></a>Comentarios

**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).

**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.

