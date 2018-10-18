---
<<<<<<< Título HEAD: RecordCount (propiedad) (ADO) TOCTitle: RecordCount (propiedad) (ADO) === título: RecordCount (propiedad, ADO) TOCTitle: RecordCount (propiedad, ADO)
>>>>>>> Master ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID: ms.date 48548304: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="recordcount-property-ado"></a>RecordCount (propiedad, ADO)
=======
# <a name="recordcount-property-ado"></a>RecordCount (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el número de registros de un objeto [Recordset](recordset-object-ado.md).

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **Long** que indica el número de registros del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use la propiedad **RecordCount** para descubrir cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o el tipo de cursor no admite la propiedad **RecordCount**. Al leer la propiedad **RecordCount** en un objeto **Recordset** cerrado se produce un error.

Si el objeto **Recordset** es compatible con un posicionamiento aproximado o con marcadores, es decir, **Supports (adApproxPosition)** o **Supports (adBookmark)** devuelven respectivamente **True**, este valor será el número exacto de registros en el objeto **Recordset**, independientemente de si se ha rellenado por completo. Si el objeto **Recordset** no es compatible con un posicionamiento aproximado, esta propiedad puede suponer una considerable pérdida de recursos, dado que será necesario recuperar y contar todos los registros para devolver un valor de **RecordCount** preciso.

El tipo de cursor del objeto **Recordset** afecta a la posibilidad de determinar el número de registros. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves y -1 o el recuento real para un cursor dinámico, según el origen de datos.

