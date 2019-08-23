---
title: Información sobre cómo establecer el orden de resolución de las listas de direcciones en Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321836"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="00852-103">Información sobre cómo establecer el orden de resolución de las listas de direcciones en Outlook</span><span class="sxs-lookup"><span data-stu-id="00852-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="00852-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00852-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00852-105">Para cada perfil, Microsoft Office Outlook admite varias listas de direcciones y los usuarios pueden especificar manualmente el orden de las listas de direcciones por las que se resuelven los destinatarios de correo electrónico y los asistentes de las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="00852-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="00852-106">Por ejemplo, puede establecer el orden de resolución para que los nombres se resuelvan primero en la libreta de direcciones de Outlook y, a continuación, en la lista Global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="00852-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="00852-107">En un ordenador, un usuario puede abrir la libreta de direcciones, hacer clic en **Herramientas** y **Opciones** para especificar el orden de resolución.</span><span class="sxs-lookup"><span data-stu-id="00852-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="00852-108">Sin embargo, en un entorno corporativo, es más eficaz que los administradores de TI establezcan mediante programación el orden de las listas de direcciones por las que se resuelven los nombres.</span><span class="sxs-lookup"><span data-stu-id="00852-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="00852-109">Dicho código puede usarse como parte de un script de automatización de inicio que un administrador implemente en la organización.</span><span class="sxs-lookup"><span data-stu-id="00852-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="00852-p102">MAPI es compatible con el método **[SetSearchPath](iaddrbook-getsearchpath.md)** de la interfaz **[IAddrBook](iaddrbookimapiprop.md)**, que le permite establecer una nueva ruta de búsqueda en el perfil que se usa para la resolución de nombres. Para usar el método **IAddrBook::SetSearchPath**, debe especificar el orden de resolución deseado a través de una matriz que contiene los contenedores de las libretas de direcciones relevantes en el orden en que deben resolverse. Cada entrada de la matriz también debe contener el identificador de entrada de la libreta de direcciones correspondiente.</span><span class="sxs-lookup"><span data-stu-id="00852-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="00852-113">Los siguientes son ejemplos de código sobre cómo especificar una ruta de búsqueda personalizada para las listas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="00852-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="00852-114">Establecer mediante programación el orden de resolución para las listas de direcciones</span><span class="sxs-lookup"><span data-stu-id="00852-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="00852-115">KB 292590: Cómo cambiar el orden de clasificación de la libreta de direcciones con SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="00852-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

