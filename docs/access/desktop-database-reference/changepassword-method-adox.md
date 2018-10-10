---
title: ChangePassword (método, ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483668"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="5a504-102">ChangePassword (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="5a504-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="5a504-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a504-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="5a504-104">Cambia la contraseña de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5a504-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a504-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a504-105">Syntax</span></span>

<span data-ttu-id="5a504-106">*Usuario*. ChangePassword*contraseñaAntigua*, *nuevaContraseña*</span><span class="sxs-lookup"><span data-stu-id="5a504-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="5a504-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a504-107">Parameters</span></span>

  - <span data-ttu-id="5a504-108">*ContraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="5a504-108">*OldPassword*</span></span>

  - <span data-ttu-id="5a504-p101">Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="5a504-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="5a504-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="5a504-111">*NewPassword*</span></span>

  - <span data-ttu-id="5a504-112">Un valor **String** que especifica la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="5a504-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a504-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a504-113">Remarks</span></span>

<span data-ttu-id="5a504-114">Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.</span><span class="sxs-lookup"><span data-stu-id="5a504-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="5a504-115">Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="5a504-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

