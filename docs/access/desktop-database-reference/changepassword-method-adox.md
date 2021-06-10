---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296531"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="9207e-102">Método ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9207e-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="9207e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9207e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9207e-104">Cambia la contraseña de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="9207e-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="9207e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9207e-105">Syntax</span></span>

<span data-ttu-id="9207e-106">*Usuario*. ChangePassword *OldPassword*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="9207e-106">*User*.ChangePassword *OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="9207e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9207e-107">Parameters</span></span>

|<span data-ttu-id="9207e-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9207e-108">Parameter</span></span>|<span data-ttu-id="9207e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9207e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9207e-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="9207e-110">*OldPassword*</span></span> |<span data-ttu-id="9207e-p101">Un valor **String** que especifica la contraseña existente del usuario. Si el usuario no tiene contraseña todavía, utilice una cadena vacía ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="9207e-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="9207e-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="9207e-113">*NewPassword*</span></span> |<span data-ttu-id="9207e-114">Un valor **String** que especifica la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="9207e-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9207e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9207e-115">Remarks</span></span>

<span data-ttu-id="9207e-116">Por motivos de seguridad, se debe especificar la contraseña antigua además de la nueva.</span><span class="sxs-lookup"><span data-stu-id="9207e-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="9207e-117">Si el proveedor no admite la administración de propiedades de confianza, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="9207e-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

