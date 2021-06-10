---
title: Append (método, Groups de ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297105"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="91b53-102">Append (método, Groups de ADOX)</span><span class="sxs-lookup"><span data-stu-id="91b53-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="91b53-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91b53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91b53-104">Agrega un nuevo objeto [Group](group-object-adox.md) a la colección [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="91b53-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91b53-105">Syntax</span></span>

<span data-ttu-id="91b53-106">*Grupos*. Grupo Append</span><span class="sxs-lookup"><span data-stu-id="91b53-106">*Groups*.Append *Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="91b53-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91b53-107">Parameters</span></span>

|<span data-ttu-id="91b53-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="91b53-108">Parameter</span></span>|<span data-ttu-id="91b53-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="91b53-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="91b53-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="91b53-110">*Group*</span></span> |<span data-ttu-id="91b53-111">El objeto **Group** que se anexará o el nombre del grupo que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="91b53-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="91b53-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91b53-112">Remarks</span></span>

<span data-ttu-id="91b53-p101">La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="91b53-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="91b53-115">Si el proveedor no admite la creación de grupos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="91b53-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="91b53-116">[!NOTA] Para poder anexar un objeto **Group** a la colección **Groups** de un objeto **User**, debe existir previamente un objeto **Group** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Groups** del **catálogo**.</span><span class="sxs-lookup"><span data-stu-id="91b53-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


