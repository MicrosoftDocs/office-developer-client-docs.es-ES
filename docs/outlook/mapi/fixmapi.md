---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816812"
---
# <a name="fixmapi"></a><span data-ttu-id="fe06d-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="fe06d-103">FixMAPI</span></span>

  
  
<span data-ttu-id="fe06d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe06d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe06d-105">Realiza una copia de seguridad de la copia actual de mapi32.dll en el cliente de equipo y restaura mapi32.dll con la biblioteca de código auxiliar MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="fe06d-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fe06d-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="fe06d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe06d-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="fe06d-107">Exported by:</span></span>  <br/> |<span data-ttu-id="fe06d-108">MAPISTUB.dll</span><span class="sxs-lookup"><span data-stu-id="fe06d-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="fe06d-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fe06d-109">Called by:</span></span>  <br/> |<span data-ttu-id="fe06d-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="fe06d-110">Client</span></span>  <br/> |
|<span data-ttu-id="fe06d-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="fe06d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe06d-112">Windows</span><span class="sxs-lookup"><span data-stu-id="fe06d-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="fe06d-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fe06d-113">Return values</span></span>

<span data-ttu-id="fe06d-114">Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fe06d-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="fe06d-115">Si se produce un error en la función, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="fe06d-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="fe06d-116">Para obtener información de error extendida, llame a la función del Kit de desarrollo de Software (SDK) de Microsoft Windows, **[GetLastError](http://msdn.microsoft.com/es-es/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="fe06d-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/es-es/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe06d-117">Notas</span><span class="sxs-lookup"><span data-stu-id="fe06d-117">Remarks</span></span>

 <span data-ttu-id="fe06d-118">**FixMAPI** no reemplazar el archivo mapi32.dll actual si el archivo está marcado como de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe06d-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="fe06d-119">**FixMAPI** no reemplazar el archivo mapi32.dll actual si Microsoft Exchange Server está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fe06d-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="fe06d-120">Cuando **FixMAPI** realiza una copia de seguridad de la copia actual de mapi32.dll en el equipo, asigna a la copia un nombre distinto de "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="fe06d-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="fe06d-121">A continuación, dirige las llamadas subsiguientes destinadas a ese ensamblado a la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fe06d-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe06d-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="fe06d-122">See also</span></span>



[<span data-ttu-id="fe06d-123">KB 256946: Recibe un mensaje de error de conflicto de programa al iniciar Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="fe06d-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="fe06d-124">KB 228457: Descripción de la herramienta Fixmapi.exe incluidos con Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="fe06d-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

