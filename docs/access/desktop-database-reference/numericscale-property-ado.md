---
<<<<<<< Título HEAD: NumericScale (propiedad) (ADO) TOCTitle: NumericScale (propiedad) (ADO) === título: NumericScale (propiedad, ADO) TOCTitle: NumericScale (propiedad, ADO)
>>>>>>> Master ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: ms.date 48544824: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="numericscale-property-ado"></a>NumericScale (propiedad, ADO)
=======
# <a name="numericscale-property-ado"></a>NumericScale (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica la escala de valores numéricos de un objeto [Parameter](parameter-object-ado.md) o [Field](field-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Byte** que indica el número de posiciones decimales en las que se resolverán los valores numéricos.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **NumericScale** para determinar cuántos dígitos a la derecha de la coma decimal se utilizarán para representar valores de un objeto numérico **Parameter** o **Field**.

En los objetos **Parameter**, la propiedad **NumericScale** es de lectura y escritura.

En un objeto **Field**, **NumericScale** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **NumericScale** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

