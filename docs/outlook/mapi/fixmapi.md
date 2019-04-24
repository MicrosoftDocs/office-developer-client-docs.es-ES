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
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334964"
---
# <a name="fixmapi"></a><span data-ttu-id="527c3-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="527c3-103">FixMAPI</span></span>

  
  
<span data-ttu-id="527c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="527c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="527c3-105">Realiza una copia de seguridad de la copia actual de Mapi32. dll en el equipo cliente y restaura Mapi32. dll con la biblioteca de código auxiliar de MAPI, MAPISTUB. dll.</span><span class="sxs-lookup"><span data-stu-id="527c3-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="527c3-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="527c3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="527c3-107">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="527c3-107">Exported by:</span></span>  <br/> |<span data-ttu-id="527c3-108">MAPISTUB. dll</span><span class="sxs-lookup"><span data-stu-id="527c3-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="527c3-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="527c3-109">Called by:</span></span>  <br/> |<span data-ttu-id="527c3-110">Client</span><span class="sxs-lookup"><span data-stu-id="527c3-110">Client</span></span>  <br/> |
|<span data-ttu-id="527c3-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="527c3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="527c3-112">Windows</span><span class="sxs-lookup"><span data-stu-id="527c3-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="527c3-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="527c3-113">Return values</span></span>

<span data-ttu-id="527c3-114">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="527c3-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="527c3-115">Si se produce un error en la función, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="527c3-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="527c3-116">Para obtener información ampliada del error, llame a la función del kit de desarrollo de software (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="527c3-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="527c3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="527c3-117">Remarks</span></span>

 <span data-ttu-id="527c3-118">**FixMAPI** no reemplaza el archivo Mapi32. dll actual si el archivo está marcado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="527c3-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="527c3-119">**FixMAPI** no reemplaza el archivo Mapi32. dll actual si Microsoft Exchange Server está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="527c3-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="527c3-120">Cuando **FixMAPI** hace una copia de seguridad de la copia actual de Mapi32. dll en el equipo, asigna a la copia de seguridad un nombre distinto de "Mapi32. dll".</span><span class="sxs-lookup"><span data-stu-id="527c3-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="527c3-121">A continuación, dirige las llamadas posteriores dirigidas a ese ensamblado a la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="527c3-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="527c3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="527c3-122">See also</span></span>



[<span data-ttu-id="527c3-123">KB 256946: recibe un mensaje de error de conflicto de programas al iniciar Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="527c3-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="527c3-124">KB 228457: Descripción de la herramienta Fixmapi. exe que se incluye con Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="527c3-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

