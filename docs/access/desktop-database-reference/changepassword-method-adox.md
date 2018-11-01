---
title: ChangePassword (método, ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34de673d29d160c715c8e2617d0e2a75e3843904
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872238"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="ca7ab-102">ChangePassword (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="ca7ab-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="ca7ab-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca7ab-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ca7ab-104">Cambia la contraseña de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca7ab-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca7ab-105">Syntax</span></span>

<span data-ttu-id="ca7ab-106">*Usuario*. ChangePassword*contraseñaAntigua*, *nuevaContraseña*</span><span class="sxs-lookup"><span data-stu-id="ca7ab-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="ca7ab-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca7ab-107">Parameters</span></span>

  - <span data-ttu-id="ca7ab-108">*ContraseñaAntigua*</span><span class="sxs-lookup"><span data-stu-id="ca7ab-108">*OldPassword*</span></span>

  - <span data-ttu-id="ca7ab-p101">Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="ca7ab-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="ca7ab-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="ca7ab-111">*NewPassword*</span></span>

  - <span data-ttu-id="ca7ab-112">Un valor **String** que especifica la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="ca7ab-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca7ab-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca7ab-113">Remarks</span></span>

<span data-ttu-id="ca7ab-114">Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.</span><span class="sxs-lookup"><span data-stu-id="ca7ab-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="ca7ab-115">Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ca7ab-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

