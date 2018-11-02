---
title: Append (método, Groups de ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfc2da5490cf5c148d39670dedfb2551cedd31f2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923591"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="e47e2-102">Append (método, Groups de ADOX)</span><span class="sxs-lookup"><span data-stu-id="e47e2-102">Append method (ADOX Groups)</span></span>


<span data-ttu-id="e47e2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e47e2-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e47e2-104">Agrega un nuevo objeto [Group](group-object-adox.md) a la colección [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e47e2-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e47e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e47e2-105">Syntax</span></span>

<span data-ttu-id="e47e2-106">*Grupos*. Anexe el*grupo*</span><span class="sxs-lookup"><span data-stu-id="e47e2-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="e47e2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e47e2-107">Parameters</span></span>

  - <span data-ttu-id="e47e2-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="e47e2-108">*Group*</span></span>

  - <span data-ttu-id="e47e2-109">El objeto **Group** que se anexará o el nombre del grupo que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="e47e2-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="e47e2-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e47e2-110">Remarks</span></span>

<span data-ttu-id="e47e2-p101">La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="e47e2-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="e47e2-113">Si el proveedor no admite la creación de grupos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e47e2-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="e47e2-114">[!NOTA] Para poder anexar un objeto **Group** a la colección **Groups** de un objeto **User**, debe existir previamente un objeto **Group** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Groups** del **catálogo**.</span><span class="sxs-lookup"><span data-stu-id="e47e2-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


