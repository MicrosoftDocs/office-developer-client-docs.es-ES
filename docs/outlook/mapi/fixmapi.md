---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 863e401f66a8012b3bd9954ed56c02382f1bd4e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565939"
---
# <a name="fixmapi"></a><span data-ttu-id="56e98-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="56e98-103">FixMAPI</span></span>

  
  
<span data-ttu-id="56e98-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56e98-105">Realiza una copia de seguridad de la copia actual de mapi32.dll en el cliente de equipo y restaura mapi32.dll con la biblioteca de código auxiliar MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="56e98-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56e98-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="56e98-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56e98-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="56e98-107">Exported by:</span></span>  <br/> |<span data-ttu-id="56e98-108">MAPISTUB.dll</span><span class="sxs-lookup"><span data-stu-id="56e98-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="56e98-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="56e98-109">Called by:</span></span>  <br/> |<span data-ttu-id="56e98-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="56e98-110">Client</span></span>  <br/> |
|<span data-ttu-id="56e98-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="56e98-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="56e98-112">Windows</span><span class="sxs-lookup"><span data-stu-id="56e98-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="56e98-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="56e98-113">Return values</span></span>

<span data-ttu-id="56e98-114">Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="56e98-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="56e98-115">Si se produce un error en la función, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="56e98-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="56e98-116">Para obtener información de error extendida, llame a la función del Kit de desarrollo de Software (SDK) de Microsoft Windows, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="56e98-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56e98-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56e98-117">Remarks</span></span>

 <span data-ttu-id="56e98-118">**FixMAPI** no reemplazar el archivo mapi32.dll actual si el archivo está marcado como de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="56e98-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="56e98-119">**FixMAPI** no reemplazar el archivo mapi32.dll actual si Microsoft Exchange Server está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="56e98-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="56e98-120">Cuando **FixMAPI** realiza una copia de seguridad de la copia actual de mapi32.dll en el equipo, asigna a la copia un nombre distinto de "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="56e98-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="56e98-121">A continuación, dirige las llamadas subsiguientes destinadas a ese ensamblado a la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="56e98-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56e98-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="56e98-122">See also</span></span>



[<span data-ttu-id="56e98-123">KB 256946: Recibe un mensaje de error de conflicto de programa al iniciar Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="56e98-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="56e98-124">KB 228457: Descripción de la herramienta Fixmapi.exe incluidos con Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="56e98-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

