---
title: Bibliotecas de formularios de carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f5ce900fee3d40a46e66ac8f74f111db33d7522e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816830"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="d4f36-103">Bibliotecas de formularios de carpeta</span><span class="sxs-lookup"><span data-stu-id="d4f36-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="d4f36-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4f36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4f36-105">En algunos casos, es posible que desee asociar uno o varios formularios a una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="d4f36-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="d4f36-106">Por ejemplo, los empleados de su organización podrían tener una carpeta de informes de progreso en su almacén de mensajes personal para crear y almacenar los informes de progreso.</span><span class="sxs-lookup"><span data-stu-id="d4f36-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="d4f36-107">Debido a que el informe de progreso es específico de informe de progreso de la carpeta de cada usuario, podría no ser apropiado almacenar el formulario de informe de progreso en la biblioteca de formulario todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="d4f36-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="d4f36-108">Sin embargo, se puede mantener una copia del formulario de informe de progreso en la tabla de contenido asociados de la carpeta de informes de progreso de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="d4f36-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="d4f36-109">Esto impide que el usuario mediante formularios de informe de progreso fuera de la carpeta designada.</span><span class="sxs-lookup"><span data-stu-id="d4f36-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="d4f36-110">Conceptualmente, hay una biblioteca de formularios de carpeta para todas las carpetas de un almacén de mensajes, incluso si no hay servidores de formulario están instaladas en ella.</span><span class="sxs-lookup"><span data-stu-id="d4f36-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="d4f36-111">Las bibliotecas de formularios de carpeta se implementan como otras bibliotecas de formularios, se almacenan como tablas de contenido asociado en el elemento de la carpeta alternativa.</span><span class="sxs-lookup"><span data-stu-id="d4f36-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="d4f36-112">Debido a que las bibliotecas de formularios de carpeta están contenidas en la carpeta, se copian junto con su carpeta primaria en las operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="d4f36-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4f36-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="d4f36-113">See also</span></span>



[<span data-ttu-id="d4f36-114">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="d4f36-114">MAPI Forms</span></span>](mapi-forms.md)

