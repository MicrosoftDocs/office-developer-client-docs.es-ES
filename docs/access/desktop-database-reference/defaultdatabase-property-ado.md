---
<<<<<<< Título HEAD: DefaultDatabase (propiedad) (ADO) TOCTitle: DefaultDatabase (propiedad) (ADO) === título: DefaultDatabase (propiedad, ADO) TOCTitle: DefaultDatabase (propiedad, ADO)
>>>>>>> Master ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: ms.date 48546784: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase (propiedad, ADO)
=======
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica la base de datos predeterminada de un objeto [Connection](connection-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String** que da como resultado el nombre de una base de datos que está disponible en el proveedor.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **DefaultDatabase** para establecer o devolver el nombre de la base de datos predeterminada en un objeto **Connection** específico.

Si hay una base de datos predeterminada, puede que las cadenas SQL utilicen una sintaxis incompleta para obtener acceso a los objetos de esa base de datos. Para obtener acceso a los objetos de una base de datos distinta de la especificada en la propiedad **DefaultDatabase**, los nombres de objeto deben incluir el nombre de la base de datos deseada. Tras establecer la conexión, el proveedor escribirá la información de la base de datos predeterminada en la propiedad **DefaultDatabase**. Algunos proveedores permiten sólo una base de datos por conexión, en cuyo caso no se puede cambiar el valor de la propiedad **DefaultDatabase**.

Es posible que algunos orígenes de datos y proveedores no admitan esta característica y devuelvan un error o una cadena vacía.

**Uso de servicio de datos remotos** Esta propiedad no está disponible en un objeto de **conexión** de cliente.

