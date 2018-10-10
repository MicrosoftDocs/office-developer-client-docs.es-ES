---
title: Append (método, procedimientos ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483685"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="db20a-102">Append (método, procedimientos ADOX)</span><span class="sxs-lookup"><span data-stu-id="db20a-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="db20a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="db20a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="db20a-104">Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="db20a-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="db20a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db20a-105">Syntax</span></span>

<span data-ttu-id="db20a-106">*Los procedimientos*. Anexe el*nombre*, *comando*</span><span class="sxs-lookup"><span data-stu-id="db20a-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="db20a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db20a-107">Parameters</span></span>

  - <span data-ttu-id="db20a-108">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="db20a-108">*Name*</span></span>

  - <span data-ttu-id="db20a-109">Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="db20a-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="db20a-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="db20a-110">*Command*</span></span>

  - <span data-ttu-id="db20a-111">Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="db20a-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="db20a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db20a-112">Remarks</span></span>

<span data-ttu-id="db20a-113">Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="db20a-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="db20a-p101">Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="db20a-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="db20a-116">Cuando se usa el proveedor OLE DB para Microsoft Jet, el método <STRONG>Append</STRONG> de la colección de <STRONG>procedimientos</STRONG> le permitirá especificar una <STRONG>vista</STRONG> en lugar de un <STRONG>procedimiento</STRONG> en el parámetro <EM>Command</EM> .</span><span class="sxs-lookup"><span data-stu-id="db20a-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="db20a-117">La <STRONG>vista</STRONG> se agregará al origen de datos y a la colección <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="db20a-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="db20a-118">Después del proceso <STRONG>Append</STRONG>, si se actualizan las colecciones <STRONG>Procedures</STRONG> y <STRONG>Views</STRONG>, la <STRONG>vista</STRONG> ya no existirá en la colección <STRONG>Procedures</STRONG> y aparecerá en la colección <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="db20a-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>


