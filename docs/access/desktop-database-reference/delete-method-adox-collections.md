---
title: Método Delete (colecciones de ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708637"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="0642b-102">Método Delete (colecciones de ADOX)</span><span class="sxs-lookup"><span data-stu-id="0642b-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="0642b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0642b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0642b-104">Quita un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="0642b-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0642b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0642b-105">Syntax</span></span>

<span data-ttu-id="0642b-106">*Colección*. Eliminar*nombre*</span><span class="sxs-lookup"><span data-stu-id="0642b-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="0642b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0642b-107">Parameters</span></span>

|<span data-ttu-id="0642b-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0642b-108">Parameter</span></span>|<span data-ttu-id="0642b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0642b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0642b-110">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="0642b-110">*Name*</span></span> |<span data-ttu-id="0642b-111">Un valor **Variant** que especifica el nombre o la posición ordinal (índice) del objeto que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="0642b-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0642b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0642b-112">Remarks</span></span>

<span data-ttu-id="0642b-113">Se producirá un error si el *nombre* no existe en la colección.</span><span class="sxs-lookup"><span data-stu-id="0642b-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="0642b-p101">Para colecciones [Tables](tables-collection-adox.md) y [Users](users-collection-adox.md), se producirá un error si el proveedor no admite la eliminación de tablas o de usuarios, respectivamente. Para colecciones [Procedures](procedures-collection-adox.md) y [Views](views-collection-adox.md), se producirá un error en **Delete** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="0642b-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

