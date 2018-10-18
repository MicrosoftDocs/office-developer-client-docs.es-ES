---
<<<<<<< Título HEAD: descripción (propiedad) (ADO) TOCTitle: descripción (propiedad) (ADO) === título: descripción (propiedad, ADO) TOCTitle: descripción (propiedad, ADO)
>>>>>>> Master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: ms.date 48544064: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="description-property-ado"></a>Description (propiedad, ADO)
=======
# <a name="description-property-ado"></a>Descripción (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Describe un objeto [Error](error-object-ado.md).

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **String** que contiene una descripción del error.

## <a name="remarks"></a>Comentarios

Use la propiedad **Description** para obtener una breve descripción del error. Muestre esta propiedad para alertar al usuario sobre un error que no puede o no desea controlar. La cadena procederá de ADO o de un proveedor.

Los proveedores son responsables de especificar el texto del error específico a ADO. ADO agrega un objeto [Error](error-object-ado.md) a la colección **Errors** por cada error o advertencia que recibe del proveedor. Enumere la colección **Errors** para rastrear los errores que especifica el proveedor.

