---
title: Append (método, usuarios ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484130"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="dcd70-102">Append (método, usuarios ADOX)</span><span class="sxs-lookup"><span data-stu-id="dcd70-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="dcd70-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcd70-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="dcd70-104">Agrega un nuevo objeto [User](user-object-adox.md) a la colección [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="dcd70-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd70-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcd70-105">Syntax</span></span>

<span data-ttu-id="dcd70-106">*Los usuarios*. Anexe el*usuario*\[,*contraseña*\]</span><span class="sxs-lookup"><span data-stu-id="dcd70-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="dcd70-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcd70-107">Parameters</span></span>

  - <span data-ttu-id="dcd70-108">*User*</span><span class="sxs-lookup"><span data-stu-id="dcd70-108">*User*</span></span>

  - <span data-ttu-id="dcd70-109">Un valor **Variant** que contiene el objeto **User** que se va a anexar o al nombre del usuario que se va a crear y anexar.</span><span class="sxs-lookup"><span data-stu-id="dcd70-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="dcd70-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="dcd70-110">*Password*</span></span>

  - <span data-ttu-id="dcd70-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dcd70-111">Optional.</span></span> <span data-ttu-id="dcd70-112">Un valor **String** que contiene la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="dcd70-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="dcd70-113">El parámetro *Password* corresponde al valor especificado por el método [ChangePassword](changepassword-method-adox.md) de un objeto de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="dcd70-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd70-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dcd70-114">Remarks</span></span>

<span data-ttu-id="dcd70-p102">La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.</span><span class="sxs-lookup"><span data-stu-id="dcd70-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="dcd70-117">Si el proveedor no admite la creación de usuarios, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="dcd70-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dcd70-118">[!NOTA] Para poder anexar un objeto <STRONG>User</STRONG> a la colección <STRONG>Users</STRONG> de un objeto <STRONG>Group</STRONG>, debe existir previamente un objeto <STRONG>User</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Users</STRONG> del <STRONG>catálogo</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="dcd70-118">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


