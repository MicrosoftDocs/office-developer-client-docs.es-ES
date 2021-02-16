---
title: Bibliotecas de formularios de carpetas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414287"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="217a2-103">Bibliotecas de formularios de carpetas</span><span class="sxs-lookup"><span data-stu-id="217a2-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="217a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="217a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="217a2-105">En algunos casos, es posible que desee asociar uno o más formularios a una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="217a2-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="217a2-106">Por ejemplo, los empleados de la organización podrían tener una carpeta Informe de progreso en su almacén de mensajes personales para crear y almacenar informes de progreso.</span><span class="sxs-lookup"><span data-stu-id="217a2-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="217a2-107">Dado que el informe de progreso es específico de la carpeta Informe de progreso de cada usuario, puede que no sea adecuado almacenar el formulario de informe de progreso en la biblioteca de formularios de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="217a2-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="217a2-108">Sin embargo, se puede conservar una copia del formulario de informe de progreso en la tabla de contenido asociado de la carpeta Informe de progreso de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="217a2-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="217a2-109">Esto restringe al usuario el uso de formularios de informe de progreso fuera de la carpeta designada.</span><span class="sxs-lookup"><span data-stu-id="217a2-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="217a2-110">Conceptualmente, hay una biblioteca de formularios de carpeta para cada carpeta de un almacén de mensajes, incluso si no hay ningún servidor de formulario instalado en él.</span><span class="sxs-lookup"><span data-stu-id="217a2-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="217a2-111">Las bibliotecas de formularios de carpetas se implementan como otras bibliotecas de formularios: se almacenan como tablas de contenido asociado en la parte alternativa de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="217a2-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="217a2-112">Dado que las bibliotecas de formularios de carpetas están contenidas en la carpeta, se copian junto con su carpeta principal en las operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="217a2-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="217a2-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="217a2-113">See also</span></span>



[<span data-ttu-id="217a2-114">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="217a2-114">MAPI Forms</span></span>](mapi-forms.md)

