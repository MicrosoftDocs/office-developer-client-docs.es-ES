---
<<<<<<< Título HEAD: tipo (propiedad) (ADO) TOCTitle: tipo de propiedad (ADO) === título: escriba (propiedad, ADO) TOCTitle: escriba (propiedad, ADO)
>>>>>>> Master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: ms.date 48543397: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="type-property-ado"></a>Type (propiedad, ADO)
=======
# <a name="type-property-ado"></a>Tipo (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el tipo operativo o tipo de datos de un objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) o [Property](property-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Comentarios

En objetos **Parameter**, la propiedad **Type** es de lectura y escritura. En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Type** sólo es de lectura y escritura después de que se haya especificado la propiedad [Value](value-property-ado.md) del objeto **Field** y el proveedor de datos haya agregado correctamente el nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

En el resto de los objetos, la propiedad **Type** es de sólo lectura.

