---
title: Acerca de c�mo establecer el orden de resoluci�n para las listas de direcciones en Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816350"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="9a0f4-103">Acerca de c�mo establecer el orden de resoluci�n para las listas de direcciones en Outlook</span><span class="sxs-lookup"><span data-stu-id="9a0f4-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="9a0f4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a0f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a0f4-105">Para cada perfil, Microsoft Office Outlook es compatible con varias listas de direcciones y los usuarios pueden especificar manualmente el orden de las listas de direcciones por qué los destinatarios de correo electrónico se resuelven los mensajes y los asistentes de las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="9a0f4-106">Por ejemplo, puede establecer el orden de resoluci�n para que los nombres se resuelven primero en su libreta de direcciones de Outlook y a continuaci�n, en la lista Global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="9a0f4-107">En un equipo, un usuario puede abrir la libreta de direcciones, haga clic en **Herramientas** y, a continuaci�n, en **Opciones** para especificar el orden de resoluci�n.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="9a0f4-108">Sin embargo, en un entorno corporativo, es m�s eficaz para los administradores de TI establecer mediante programaci�n el orden de las listas de direcciones mediante el cual se resuelven nombres.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="9a0f4-109">Este c�digo puede utilizarse como parte de una secuencia de comandos de automatizaci�n de inicio que un administrador implementa dentro de la corporaci�n.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="9a0f4-p102">MAPI es compatible con el m�todo **[SetSearchPath](iaddrbook-getsearchpath.md)** en la interfaz **[IAddrBook](iaddrbookimapiprop.md)**, que le permite establecer una nueva ruta de b�squeda en el perfil que se usa para la resoluci�n de nombres. Para usar el m�todo **IAddrBook::SetSearchPath**, debe especificar el orden de resoluci�n que desee mediante el uso de una matriz que contiene los contenedores de la direcci�n relevante de libros en el orden en que se deben resolver. Cada entrada de la matriz tambi�n debe contener el identificador de entrada de la libreta de direcciones correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="9a0f4-113">Los siguientes son ejemplos de c�digo de c�mo especificar una ruta de acceso de b�squeda personalizada para las listas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="9a0f4-114">Establecer mediante programación el orden de resolución para las listas de direcciones</span><span class="sxs-lookup"><span data-stu-id="9a0f4-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="9a0f4-115">KB 292590: c�mo cambiar el orden de ordenaci�n de la libreta de direcciones con SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9a0f4-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

