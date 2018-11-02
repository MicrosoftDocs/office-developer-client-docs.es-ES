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
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592930"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="fa015-103">Implementar una interfaz de configuración para los proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa015-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="fa015-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa015-105">Los proveedores de almacén de mensajes son necesarios para implementar una interfaz que permite al usuario configurar el proveedor de almacenamiento de mensajes para que se ejecute en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="fa015-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="fa015-106">Normalmente, se configura el proveedor de almacén de mensajes cuando se agrega el proveedor de almacenamiento de mensajes a un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="fa015-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="fa015-107">Interfaz de configuración del proveedor de almacén de mensajes generalmente controla las tareas como la configuración de los nombres de usuario y contraseñas para almacenes de mensaje protegido, selección de rutas de acceso a los archivos necesarios, y crear el mecanismo de almacenamiento subyacente va a utilizar, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="fa015-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="fa015-108">Se obtiene acceso a la interfaz de configuración que se implementa a través de puntos de entrada adicionales en el archivo DLL del proveedor de servicio mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa015-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="fa015-109">Para obtener más información, vea [configurar un servicio de mensajes](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="fa015-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="fa015-110">Interfaz de configuración del proveedor de almacén de mensajes es la única interfaz de usuario que debe implementar un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fa015-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa015-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa015-111">See also</span></span>



[<span data-ttu-id="fa015-112">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa015-112">Message Store Features</span></span>](message-store-features.md)

