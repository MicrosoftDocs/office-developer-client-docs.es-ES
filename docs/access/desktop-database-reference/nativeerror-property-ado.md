---
<<<<<<< Título HEAD: NativeError (propiedad) (ADO) TOCTitle: NativeError (propiedad) (ADO) === título: NativeError (propiedad, ADO) TOCTitle: NativeError (propiedad, ADO)
>>>>>>> Master ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: ms.date 48546685: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="nativeerror-property-ado"></a>NativeError (propiedad, ADO)
=======
# <a name="nativeerror-property-ado"></a>NativeError (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el código de error específico de un proveedor para un objeto [Error](error-object-ado.md) dado.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **Long** que indica el código del error.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **NativeError** para recuperar información de error específica de base de datos de un objeto **Error** concreto. Por ejemplo, al utilizar el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error nativos que se originan en SQL Server pasan a través de ODBC y el Proveedor ODBC a la propiedad **NativeError** de ADO.

