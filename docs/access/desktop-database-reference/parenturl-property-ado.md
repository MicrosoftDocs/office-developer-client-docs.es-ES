---
<span data-ttu-id="4aca5-101"><<<<<<< Título HEAD: ParentURL (propiedad) (ADO) TOCTitle: ParentURL (propiedad) (ADO) === título: ParentURL (propiedad, ADO) TOCTitle: ParentURL (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4aca5-101"><<<<<<< HEAD title: ParentURL Property (ADO) TOCTitle: ParentURL Property (ADO) ======= title: ParentURL property (ADO) TOCTitle: ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4aca5-102">Master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: ms.date 48548517: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="4aca5-102">master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4aca5-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4aca5-103"><<<<<<< HEAD</span></span>
# <a name="parenturl-property-ado"></a><span data-ttu-id="4aca5-104">ParentURL (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4aca5-104">ParentURL Property (ADO)</span></span>
=======
# <a name="parenturl-property-ado"></a><span data-ttu-id="4aca5-105">ParentURL (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4aca5-105">ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4aca5-106">master</span><span class="sxs-lookup"><span data-stu-id="4aca5-106">master</span></span>

<span data-ttu-id="4aca5-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4aca5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4aca5-108">Indica una cadena URL absoluta que apunta al objeto [Record](record-object-ado.md) primario del objeto **Record** actual.</span><span class="sxs-lookup"><span data-stu-id="4aca5-108">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

<span data-ttu-id="4aca5-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4aca5-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="4aca5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aca5-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="4aca5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aca5-111">Return value</span></span>
>>>>>>> <span data-ttu-id="4aca5-112">master</span><span class="sxs-lookup"><span data-stu-id="4aca5-112">master</span></span>

<span data-ttu-id="4aca5-113">Devuelve un valor de tipo **String** que indica la dirección URL del objeto **Record** primario.</span><span class="sxs-lookup"><span data-stu-id="4aca5-113">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aca5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4aca5-114">Remarks</span></span>

<span data-ttu-id="4aca5-p101">La propiedad **ParentURL** depende del origen usado para abrir el objeto **Record**. Por ejemplo, **Record** se puede abrir mediante un origen que contenga el nombre de ruta de acceso relativa de un directorio al que se hace referencia por medio de la propiedad [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4aca5-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="4aca5-p102">Imagine que "second" es una carpeta incluida en "first". Abra el objeto **Record** mediante el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="4aca5-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="4aca5-119">Ahora, el valor de la propiedad **ParentURL** es la propiedad **ParentURL** es "https://first", al igual que **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="4aca5-119">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="4aca5-120">El origen también puede ser una dirección URL absoluta, como "https://first/second".</span><span class="sxs-lookup"><span data-stu-id="4aca5-120">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="4aca5-121">La propiedad **ParentURL** es "https://first", el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4aca5-121">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="4aca5-122">La propiedad **ParentURL** es "https://first", el nivel superior "segundo".</span><span class="sxs-lookup"><span data-stu-id="4aca5-122">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="4aca5-123">Esta propiedad puede ser un valor nulo si:</span><span class="sxs-lookup"><span data-stu-id="4aca5-123">This property may be a null value if:</span></span>

- <span data-ttu-id="4aca5-124">No hay ningún elemento primario para el objeto actual; por ejemplo, si el objeto **Record** representa la raíz de un directorio.</span><span class="sxs-lookup"><span data-stu-id="4aca5-124">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="4aca5-125">El objeto **Record** representa una entidad que no se puede especificar con una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="4aca5-125">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="4aca5-126">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4aca5-126">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="4aca5-p104">[!NOTA] Esta propiedad sólo es admitida por proveedores de origen de documentos, como el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Registros y campos proporcionados por un proveedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="4aca5-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="4aca5-129">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="4aca5-129">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="4aca5-130">Para obtener más información, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="4aca5-130">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="4aca5-131">[!NOTA] Si el registro actual incluye un registro de datos de un objeto **Recordset** ADO, el acceso a la propiedad **ParentURL** provoca un error en tiempo de ejecución, lo que indica que no hay dirección URL posible.</span><span class="sxs-lookup"><span data-stu-id="4aca5-131">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


