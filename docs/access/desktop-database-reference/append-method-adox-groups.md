---
title: Append (método, grupos ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486377"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="de48c-102">Append (método, grupos ADOX)</span><span class="sxs-lookup"><span data-stu-id="de48c-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="de48c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de48c-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="de48c-104">Agrega un nuevo objeto [Group](group-object-adox.md) a la colección [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="de48c-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="de48c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de48c-105">Syntax</span></span>

<span data-ttu-id="de48c-106">*Grupos*. Anexe el*grupo*</span><span class="sxs-lookup"><span data-stu-id="de48c-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="de48c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de48c-107">Parameters</span></span>

  - <span data-ttu-id="de48c-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="de48c-108">*Group*</span></span>

  - <span data-ttu-id="de48c-109">El objeto **Group** que se anexará o el nombre del grupo que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="de48c-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="de48c-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de48c-110">Remarks</span></span>

<span data-ttu-id="de48c-p101">La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="de48c-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="de48c-113">Si el proveedor no admite la creación de grupos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="de48c-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de48c-114">[!NOTA] Para poder anexar un objeto <STRONG>Group</STRONG> a la colección <STRONG>Groups</STRONG> de un objeto <STRONG>User</STRONG>, debe existir previamente un objeto <STRONG>Group</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Groups</STRONG> del <STRONG>catálogo</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="de48c-114">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


