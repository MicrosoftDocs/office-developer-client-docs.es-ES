---
title: Implementar una interfaz de configuración para los proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817647"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="e86af-103">Implementar una interfaz de configuración para los proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="e86af-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="e86af-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e86af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e86af-105">Los proveedores de almacén de mensajes son necesarios para implementar una interfaz que permite al usuario configurar el proveedor de almacenamiento de mensajes para que se ejecute en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e86af-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="e86af-106">Normalmente, se configura el proveedor de almacén de mensajes cuando se agrega el proveedor de almacenamiento de mensajes a un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="e86af-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="e86af-107">Interfaz de configuración del proveedor de almacén de mensajes generalmente controla las tareas como la configuración de los nombres de usuario y contraseñas para almacenes de mensaje protegido, selección de rutas de acceso a los archivos necesarios, y crear el mecanismo de almacenamiento subyacente va a utilizar, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e86af-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="e86af-108">Se obtiene acceso a la interfaz de configuración que se implementa a través de puntos de entrada adicionales en el archivo DLL del proveedor de servicio mensaje.</span><span class="sxs-lookup"><span data-stu-id="e86af-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="e86af-109">Para obtener más información, vea [configurar un servicio de mensajes](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="e86af-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="e86af-110">Interfaz de configuración del proveedor de almacén de mensajes es la única interfaz de usuario que debe implementar un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e86af-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e86af-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="e86af-111">See also</span></span>



[<span data-ttu-id="e86af-112">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="e86af-112">Message Store Features</span></span>](message-store-features.md)

