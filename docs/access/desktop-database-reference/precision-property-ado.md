---
<<<<<<< Título HEAD: precisión (propiedad) (ADO) TOCTitle: precisión (propiedad) (ADO) === título: precisión (propiedad, ADO) TOCTitle: precisión (propiedad, ADO)
>>>>>>> Master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: ms.date 48547685: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="precision-property-ado"></a>Precision (propiedad, ADO)
=======
# <a name="precision-property-ado"></a>Precision (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el grado de precisión de los valores numéricos de un objeto [Parameter](parameter-object-ado.md) o de los objetos numéricos [Field](field-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Byte** que indica el número máximo de dígitos utilizado para representar valores.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Precision** para determinar el número máximo de dígitos utilizado para representar los valores de un objeto numérico **Parameter** o **Field**.

En un objeto **Parameter**, el valor es de lectura y escritura.

En un objeto **Field**, **Precision** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Precision** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

