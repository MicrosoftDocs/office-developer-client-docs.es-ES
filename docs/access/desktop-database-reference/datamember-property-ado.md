---
<<<<<<< Título HEAD: DataMember (propiedad) (ADO) TOCTitle: DataMember (propiedad) (ADO) === título: DataMember (propiedad, ADO) TOCTitle: DataMember (propiedad, ADO)
>>>>>>> Master ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: ms.date 48548787: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="datamember-property-ado"></a>DataMember (propiedad, ADO)
=======
# <a name="datamember-property-ado"></a>DataMember (propiedad, ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indica el nombre del miembro de datos que se va a recuperar del objeto al que hace referencia la propiedad [DataSource](datasource-property-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String**. El nombre no distingue entre mayúsculas y minúsculas.

## <a name="remarks"></a>Comentarios

Esta propiedad se usa para crear controles enlazados a datos con el Entorno de datos. El Entorno de datos mantiene colecciones de datos (orígenes de datos) que contienen objetos con nombre (*miembros de datos*) que se representarán como un objeto [ Recordset](recordset-object-ado.md). **

Las propiedades **DataMember** y **DataSource** deben utilizarse conjuntamente.

La propiedad **DataMember** determina cuál de los objetos especificados por la propiedad **DataSource** se va a representar como un objeto **Recordset**. El objeto **Recordset** debe estar cerrado para que se pueda establecer esta propiedad. Se genera un error si no se establece la propiedad **DataMember** antes de establecerse la propiedad **DataSource**, o bien, si el objeto especificado en la propiedad **DataSource** no reconoce el nombre de **DataMember**.

**Uso**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
