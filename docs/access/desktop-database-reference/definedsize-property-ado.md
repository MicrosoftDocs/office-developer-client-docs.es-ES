---
<<<<<<< Título HEAD: DefinedSize (propiedad) (ADO) TOCTitle: DefinedSize (propiedad) (ADO) === título: DefinedSize (propiedad, ADO) TOCTitle: DefinedSize (propiedad, ADO)
>>>>>>> Master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: ms.date 48546257: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="definedsize-property-ado"></a>DefinedSize (propiedad, ADO)
=======
# <a name="definedsize-property-ado"></a>DefinedSize (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica la capacidad de datos de un objeto [Field](field-object-ado.md).

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **Long** que refleja el tamaño definido de un campo como un número de bytes.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.

Las propiedades **DefinedSize** y [ActualSize](actualsize-property-ado.md) son diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado **adVarChar** y un valor de la propiedad **DefinedSize** de 50 que contenga un carácter único. El valor de la propiedad **ActualSize** que devuelve es la longitud del carácter único en bytes.

