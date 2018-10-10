---
title: Delete (método, colecciones ADOX)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea02f02270649783873f1f086bb9f39b804034a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486258"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="22981-102">Delete (método, colecciones ADOX)</span><span class="sxs-lookup"><span data-stu-id="22981-102">Delete Method (ADOX Collections)</span></span>


<span data-ttu-id="22981-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22981-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="22981-104">Quita un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="22981-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="22981-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22981-105">Syntax</span></span>

<span data-ttu-id="22981-106">*Colección*. Eliminar*nombre*</span><span class="sxs-lookup"><span data-stu-id="22981-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="22981-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22981-107">Parameters</span></span>

  - <span data-ttu-id="22981-108">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="22981-108">*Name*</span></span>

  - <span data-ttu-id="22981-109">Un valor **Variant** que especifica el nombre o la posición ordinal (índice) del objeto que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="22981-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="22981-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22981-110">Remarks</span></span>

<span data-ttu-id="22981-111">Se producirá un error si el *nombre* no existe en la colección.</span><span class="sxs-lookup"><span data-stu-id="22981-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="22981-p101">Para colecciones [Tables](tables-collection-adox.md) y [Users](users-collection-adox.md), se producirá un error si el proveedor no admite la eliminación de tablas o de usuarios, respectivamente. Para colecciones [Procedures](procedures-collection-adox.md) y [Views](views-collection-adox.md), se producirá un error en **Delete** si el proveedor no admite comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="22981-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

