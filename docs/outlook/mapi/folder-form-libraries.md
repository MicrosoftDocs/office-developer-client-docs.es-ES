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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281560"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="ea805-103">Bibliotecas de formularios de carpetas</span><span class="sxs-lookup"><span data-stu-id="ea805-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="ea805-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea805-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea805-105">En algunos casos, es posible que desee asociar uno o más formularios con una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="ea805-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="ea805-106">Por ejemplo, los empleados de su organización podrían tener una carpeta de informe de progreso en su almacén personal de mensajes para crear y almacenar informes de progreso.</span><span class="sxs-lookup"><span data-stu-id="ea805-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="ea805-107">Como el informe de progreso es específico de la carpeta de informes de progreso de cada usuario, puede que no sea adecuado almacenar el formulario de informe de progreso en la biblioteca de formularios de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="ea805-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="ea805-108">Sin embargo, se puede conservar una copia del formulario del informe de progreso en la tabla de contenido asociado de la carpeta de informes de progreso de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="ea805-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="ea805-109">Esto impide que el usuario Use formularios de informe de progreso fuera de la carpeta designada.</span><span class="sxs-lookup"><span data-stu-id="ea805-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="ea805-110">Conceptualmente, hay una biblioteca de formularios de carpetas para cada carpeta de un almacén de mensajes, incluso si no hay servidores de formularios instalados en ella.</span><span class="sxs-lookup"><span data-stu-id="ea805-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="ea805-111">Las bibliotecas de formularios de carpeta se implementan como otras bibliotecas de formularios, que se almacenan como tablas de contenido asociado en la parte alternativa de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ea805-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="ea805-112">Como las bibliotecas de formularios de carpeta están contenidas en la carpeta, se copian junto con la carpeta principal en operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="ea805-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea805-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea805-113">See also</span></span>



[<span data-ttu-id="ea805-114">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="ea805-114">MAPI Forms</span></span>](mapi-forms.md)

