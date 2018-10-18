---
title: Source (propiedad, Record ADO)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603388"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="f8ac6-102">Source (propiedad, Record ADO)</span><span class="sxs-lookup"><span data-stu-id="f8ac6-102">Source Property (ADO Record)</span></span>


<span data-ttu-id="f8ac6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8ac6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8ac6-104">Indica el origen de datos o el objeto representados por el objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac6-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

<span data-ttu-id="f8ac6-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f8ac6-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="f8ac6-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f8ac6-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="f8ac6-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f8ac6-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="f8ac6-108">master</span><span class="sxs-lookup"><span data-stu-id="f8ac6-108">master</span></span>

<span data-ttu-id="f8ac6-109">Establece o devuelve un valor de tipo **Variant** que indica la entidad representada por el objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-109">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ac6-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8ac6-110">Remarks</span></span>

<span data-ttu-id="f8ac6-111">La propiedad **Source** devuelve el argumento *Source* del método [Open](open-method-ado-record.md) del objeto de **registro** .</span><span class="sxs-lookup"><span data-stu-id="f8ac6-111">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="f8ac6-112">Puede incluir una cadena de dirección URL absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-112">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="f8ac6-113">Es posible usar una dirección URL absoluta sin establecer la propiedad [ActiveConnection](activeconnection-property-ado.md) para abrir directamente el objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-113">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="f8ac6-114">En este caso se crea un objeto **Connection** implícito.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-114">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="f8ac6-115">La propiedad **Source** también puede incluir una referencia a un objeto **Recordset** ya abierto, que abre un objeto **Record** que representa a la fila actual del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-115">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="f8ac6-116">La propiedad **Source** también podría incluir una referencia a un objeto [Command](command-object-ado.md) que devuelve una única fila de datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-116">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="f8ac6-p102">Si también se establece la propiedad **ActiveConnection**, la propiedad **Source** debe apuntar a algún objeto que exista en el ámbito de esa conexión. Por ejemplo, en los espacios de nombre con estructura de árbol, si la propiedad **Source** incluye una dirección URL absoluta, debe apuntar a un nodo que exista en el ámbito del nodo identificado por la dirección URL en la cadena de conexión. Si la propiedad **Source** incluye una dirección URL relativa, se valida en el contexto establecido por la propiedad **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-p102">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection. For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string. If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="f8ac6-120">La propiedad **Source** es de lectura y escritura mientras el objeto **Record** está cerrado y de sólo lectura mientras el objeto **Record** está abierto.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-120">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

<span data-ttu-id="f8ac6-121"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f8ac6-121"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="f8ac6-p103">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="f8ac6-p103">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> [!NOTE]
> <span data-ttu-id="f8ac6-124">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac6-124">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="f8ac6-125">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac6-125">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="f8ac6-126">master</span><span class="sxs-lookup"><span data-stu-id="f8ac6-126">master</span></span>


