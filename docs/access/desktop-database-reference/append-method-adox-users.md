---
title: Append (método, Users de ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297070"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="3d80f-102">Append (método, Users de ADOX)</span><span class="sxs-lookup"><span data-stu-id="3d80f-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="3d80f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d80f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d80f-104">Agrega un nuevo objeto [User](user-object-adox.md) a la colección [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="3d80f-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d80f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d80f-105">Syntax</span></span>

<span data-ttu-id="3d80f-106">*Usuarios*de. Anexar*usuario*\[,*contraseña*\]</span><span class="sxs-lookup"><span data-stu-id="3d80f-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="3d80f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d80f-107">Parameters</span></span>

|<span data-ttu-id="3d80f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d80f-108">Parameter</span></span>|<span data-ttu-id="3d80f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d80f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3d80f-110">*User*</span><span class="sxs-lookup"><span data-stu-id="3d80f-110">*User*</span></span> |<span data-ttu-id="3d80f-111">Un valor **Variant** que contiene el objeto **User** que se va a anexar o al nombre del usuario que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="3d80f-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="3d80f-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="3d80f-112">*Password*</span></span> |<span data-ttu-id="3d80f-p101">Opcional. Un valor **String** que contiene la contraseña del usuario. El parámetro *Password* corresponde al valor especificado por el método [ChangePassword](changepassword-method-adox.md) de un objeto **User**.</span><span class="sxs-lookup"><span data-stu-id="3d80f-p101">Optional. A **String** value that contains the password for the user. The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3d80f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d80f-116">Remarks</span></span>

<span data-ttu-id="3d80f-p102">La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.</span><span class="sxs-lookup"><span data-stu-id="3d80f-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="3d80f-119">Si el proveedor no admite la creación de usuarios, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="3d80f-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="3d80f-120">[!NOTA] Para poder anexar un objeto **User** a la colección **Users** de un objeto **Group**, debe existir previamente un objeto **User** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Users** del **catálogo**.</span><span class="sxs-lookup"><span data-stu-id="3d80f-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


