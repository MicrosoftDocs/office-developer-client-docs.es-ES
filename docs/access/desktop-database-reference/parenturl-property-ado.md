---
title: Propiedad ParentURL (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287720"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="c2bb0-102">Propiedad ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2bb0-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="c2bb0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2bb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2bb0-104">Indica una cadena URL absoluta que apunta al objeto [Record](record-object-ado.md) primario del objeto **Record** actual.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2bb0-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2bb0-105">Return value</span></span>

<span data-ttu-id="c2bb0-106">Devuelve un valor de tipo **String** que indica la dirección URL del objeto **Record** primario.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2bb0-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2bb0-107">Remarks</span></span>

<span data-ttu-id="c2bb0-p101">La propiedad **ParentURL** depende del origen usado para abrir el objeto **Record**. Por ejemplo, **Record** se puede abrir mediante un origen que contenga el nombre de ruta de acceso relativa de un directorio al que se hace referencia por medio de la propiedad [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c2bb0-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="c2bb0-p102">Imagine que "second" es una carpeta incluida en "first". Abra el objeto **Record** mediante el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="c2bb0-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="c2bb0-112">Ahora, el valor de la **propiedad ParentURL** es **parentURL** propiedad es https://first " " , lo mismo que **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="c2bb0-113">El origen también puede ser una dirección URL absoluta como, por ejemplo, " https://first/second " .</span><span class="sxs-lookup"><span data-stu-id="c2bb0-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="c2bb0-114">La **propiedad ParentURL** es, a continuación, https://first " " , el nivel anterior .</span><span class="sxs-lookup"><span data-stu-id="c2bb0-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="c2bb0-115">La **propiedad ParentURL** es, a continuación, https://first " " , el nivel superior a "second".</span><span class="sxs-lookup"><span data-stu-id="c2bb0-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="c2bb0-116">Esta propiedad puede ser un valor nulo si:</span><span class="sxs-lookup"><span data-stu-id="c2bb0-116">This property may be a null value if:</span></span>

- <span data-ttu-id="c2bb0-117">No hay ningún elemento primario para el objeto actual; por ejemplo, si el objeto **Record** representa la raíz de un directorio.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="c2bb0-118">El objeto **Record** representa una entidad que no se puede especificar con una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="c2bb0-119">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="c2bb0-p104">[!NOTA] Esta propiedad sólo es admitida por proveedores de origen de documentos, como el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Registros y campos proporcionados por un proveedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="c2bb0-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="c2bb0-122">[!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="c2bb0-123">Para obtener más información, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="c2bb0-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="c2bb0-124">[!NOTA] Si el registro actual incluye un registro de datos de un objeto **Recordset** ADO, el acceso a la propiedad **ParentURL** provoca un error en tiempo de ejecución, lo que indica que no hay dirección URL posible.</span><span class="sxs-lookup"><span data-stu-id="c2bb0-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


