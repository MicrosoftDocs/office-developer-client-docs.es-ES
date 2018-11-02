---
title: ChangePassword (método, ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f11cfaddc99a0e10a86e0df9a7a187c4e89fc794
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921064"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="07f34-102">ChangePassword (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="07f34-102">ChangePassword method (ADOX)</span></span>


<span data-ttu-id="07f34-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07f34-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="07f34-104">Cambia la contraseña de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="07f34-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07f34-105">Syntax</span></span>

<span data-ttu-id="07f34-106">*Usuario*. ChangePassword*contraseñaAntigua*, *nuevaContraseña*</span><span class="sxs-lookup"><span data-stu-id="07f34-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="07f34-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07f34-107">Parameters</span></span>

  - <span data-ttu-id="07f34-108">*ContraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="07f34-108">*OldPassword*</span></span>

  - <span data-ttu-id="07f34-p101">Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="07f34-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="07f34-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="07f34-111">*NewPassword*</span></span>

  - <span data-ttu-id="07f34-112">Un valor **String** que especifica la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="07f34-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f34-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07f34-113">Remarks</span></span>

<span data-ttu-id="07f34-114">Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.</span><span class="sxs-lookup"><span data-stu-id="07f34-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="07f34-115">Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="07f34-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

