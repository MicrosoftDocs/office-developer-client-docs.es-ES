---
title: Append (método, usuarios ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc8f7a2d217a25a8404765aa05bae19fdccad2c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863867"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="f3eca-102">Append (método, usuarios ADOX)</span><span class="sxs-lookup"><span data-stu-id="f3eca-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="f3eca-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3eca-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f3eca-104">Agrega un nuevo objeto [User](user-object-adox.md) a la colección [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="f3eca-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3eca-105">Syntax</span></span>

<span data-ttu-id="f3eca-106">*Los usuarios*. Anexe el*usuario*\[,*contraseña*\]</span><span class="sxs-lookup"><span data-stu-id="f3eca-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="f3eca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3eca-107">Parameters</span></span>

  - <span data-ttu-id="f3eca-108">*User*</span><span class="sxs-lookup"><span data-stu-id="f3eca-108">*User*</span></span>

  - <span data-ttu-id="f3eca-109">Un valor **Variant** que contiene el objeto **User** que se va a anexar o al nombre del usuario que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="f3eca-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="f3eca-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="f3eca-110">*Password*</span></span>

  - <span data-ttu-id="f3eca-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f3eca-111">Optional.</span></span> <span data-ttu-id="f3eca-112">Un valor **String** que contiene la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="f3eca-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="f3eca-113">El parámetro *Password* corresponde al valor especificado por el método [ChangePassword](changepassword-method-adox.md) de un objeto de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="f3eca-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3eca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3eca-114">Remarks</span></span>

<span data-ttu-id="f3eca-p102">La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.</span><span class="sxs-lookup"><span data-stu-id="f3eca-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="f3eca-117">Si el proveedor no admite la creación de usuarios, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f3eca-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <span data-ttu-id="f3eca-118">[!NOTA] Para poder anexar un objeto **User** a la colección **Users** de un objeto **Group**, debe existir previamente un objeto **User** con el mismo [nombre](name-property-adox.md) que el que se va a anexar en la colección **Users** del **catálogo**.</span><span class="sxs-lookup"><span data-stu-id="f3eca-118">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


