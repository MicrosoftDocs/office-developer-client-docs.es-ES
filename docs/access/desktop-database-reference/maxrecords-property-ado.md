---
<<<<<<< Título HEAD: MaxRecords (propiedad) (ADO) TOCTitle: MaxRecords (propiedad) (ADO) === título: MaxRecords (propiedad, ADO) TOCTitle: MaxRecords (propiedad, ADO)
>>>>>>> Master ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: ms.date 48544475: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="maxrecords-property-ado"></a>MaxRecords (propiedad, ADO)
=======
# <a name="maxrecords-property-ado"></a>MaxRecords (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el número máximo de registros que se va a devolver a un objeto [Recordset](recordset-object-ado.md) desde una consulta.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long** que indica el número máximo de registros que se va a devolver. El valor predeterminado es cero (sin límite).

## <a name="remarks"></a>Comentarios

Use la propiedad **MaxRecords** para limitar el número de registros que devuelve el proveedor desde el origen de datos. El valor predeterminado de esta propiedad es cero, lo que significa que el proveedor devuelve todos los registros solicitados.

La propiedad **MaxRecords** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y es de solo lectura cuando está abierto.

