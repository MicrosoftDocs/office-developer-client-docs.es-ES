---
title: Append (método, vistas ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485066"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="2eccb-102">Append (método, vistas ADOX)</span><span class="sxs-lookup"><span data-stu-id="2eccb-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="2eccb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2eccb-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2eccb-104">Crea un nuevo objeto [View](view-object-adox.md) y lo anexa a la colección [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="2eccb-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eccb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eccb-105">Syntax</span></span>

<span data-ttu-id="2eccb-106">*Las vistas*. Anexe el*nombre*, *comando*</span><span class="sxs-lookup"><span data-stu-id="2eccb-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="2eccb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eccb-107">Parameters</span></span>

  - <span data-ttu-id="2eccb-108">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="2eccb-108">*Name*</span></span>

  - <span data-ttu-id="2eccb-109">Un valor **String** que especifica el nombre de la vista que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2eccb-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="2eccb-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="2eccb-110">*Command*</span></span>

  - <span data-ttu-id="2eccb-111">Un objeto [Command](command-object-ado.md) de ADO que representa la vista que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="2eccb-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eccb-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2eccb-112">Remarks</span></span>

<span data-ttu-id="2eccb-113">Crea una vista nueva en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="2eccb-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="2eccb-p101">Si el texto del comando que especifica el usuario representa un procedimiento en vez de una vista, el comportamiento dependerá del proveedor. **Se producirá un error en Append** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="2eccb-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2eccb-116">Cuando se usa el proveedor OLE DB para Microsoft Jet, el método <STRONG>Append</STRONG> de la colección de <STRONG>vistas</STRONG> permiten especificar un <STRONG>procedimiento</STRONG> en lugar de una <STRONG>vista</STRONG> en el parámetro <EM>Command</EM> .</span><span class="sxs-lookup"><span data-stu-id="2eccb-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="2eccb-117">El <STRONG>procedimiento</STRONG> se agregará al origen de datos y a la colección <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2eccb-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="2eccb-118">Después del proceso <STRONG>Append</STRONG>, si se actualizan las colecciones <STRONG>Procedures</STRONG> y <STRONG>Views</STRONG>, el <STRONG>procedimiento</STRONG> ya no estará en la colección <STRONG>Views</STRONG> y aparecerá en la colección <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2eccb-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>


