---
<span data-ttu-id="b62f0-101"><<<<<<< Título HEAD: DataSource (propiedad) (ADO) TOCTitle: DataSource (propiedad) (ADO) === título: DataSource (propiedad, ADO) TOCTitle: DataSource (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b62f0-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b62f0-102">Master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: ms.date 48545087: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="b62f0-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b62f0-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b62f0-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="b62f0-104">DataSource (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b62f0-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="b62f0-105">DataSource (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b62f0-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b62f0-106">master</span><span class="sxs-lookup"><span data-stu-id="b62f0-106">master</span></span>


<span data-ttu-id="b62f0-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b62f0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b62f0-108">Indica un objeto que contiene los datos que se van a representar como un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b62f0-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b62f0-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b62f0-109">Remarks</span></span>

<span data-ttu-id="b62f0-p101">Esta propiedad se usa para crear controles enlazados a datos con el Entorno de datos. El Entorno de datos mantiene colecciones de datos (orígenes de datos) que contienen objetos con nombre (*miembros de datos*) que se representarán como un objeto \*\* Recordset\*\*. \*\*</span><span class="sxs-lookup"><span data-stu-id="b62f0-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="b62f0-112">Las propiedades [DataMember](datamember-property-ado.md) y **DataSource** deben utilizarse conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="b62f0-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="b62f0-113">El objeto al que se hace referencia debe implementar la interfaz **IDataSource** y contener una interfaz **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="b62f0-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="b62f0-114">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b62f0-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
