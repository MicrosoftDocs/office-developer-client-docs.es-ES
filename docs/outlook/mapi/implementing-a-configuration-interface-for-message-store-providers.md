---
title: Implementación de una interfaz de configuración para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332980"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="e1aa1-103">Implementación de una interfaz de configuración para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1aa1-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="e1aa1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1aa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1aa1-105">Los proveedores de almacenamiento de mensajes son necesarios para implementar una interfaz que permita al usuario configurar el proveedor de almacén de mensajes para que se ejecute en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="e1aa1-106">Normalmente, el proveedor de almacenamiento de mensajes se configura cuando el proveedor de almacenamiento de mensajes se agrega al perfil de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="e1aa1-107">La interfaz de configuración del proveedor de almacenamiento de mensajes suele controlar tareas como la configuración de nombres de usuario y contraseñas para los almacenes de mensajes protegidos, la elección de rutas de archivos necesarios y la creación del mecanismo de almacenamiento subyacente que se va a usar, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="e1aa1-108">Se obtiene acceso a la interfaz de configuración que implemente a través de puntos de entrada adicionales en la DLL del proveedor de servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="e1aa1-109">Para obtener más información, vea [configuración de un servicio de mensajes](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="e1aa1-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="e1aa1-110">La interfaz de configuración del proveedor de almacenamiento de mensajes es la única interfaz de usuario que debe implementar un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1aa1-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1aa1-111">See also</span></span>



[<span data-ttu-id="e1aa1-112">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1aa1-112">Message Store Features</span></span>](message-store-features.md)

