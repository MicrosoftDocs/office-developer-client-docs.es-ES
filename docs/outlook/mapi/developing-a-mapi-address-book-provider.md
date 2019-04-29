---
title: Desarrollar un proveedor de libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409373"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="9f36f-103">Desarrollar un proveedor de libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="9f36f-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="9f36f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f36f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f36f-105">Un proveedor de libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, a los proveedores de almacenamiento y transporte de mensajes y a MAPI.</span><span class="sxs-lookup"><span data-stu-id="9f36f-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="9f36f-106">La información de los destinatarios se organiza jerárquicamente en compartimientos de almacenamiento conocidos como contenedores.</span><span class="sxs-lookup"><span data-stu-id="9f36f-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="9f36f-107">Todas las libretas de direcciones del perfil aportan uno o varios contenedores de nivel superior, o primarios, a la libreta de direcciones MAPI, una vista integrada de la información de destinatarios de todos los proveedores de la libreta de direcciones en una sesión.</span><span class="sxs-lookup"><span data-stu-id="9f36f-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="9f36f-108">A través de la libreta de direcciones MAPI, los clientes y otros proveedores de servicios obtienen acceso a los datos de un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9f36f-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="9f36f-109">MAPI crea la libreta de direcciones integrada:</span><span class="sxs-lookup"><span data-stu-id="9f36f-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="9f36f-110">Recuperar los contenedores de nivel superior de cada proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9f36f-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="9f36f-111">Recuperar la tabla de jerarquías de cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="9f36f-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="9f36f-112">Copiando cada tabla de jerarquía en una tabla de jerarquía integrada.</span><span class="sxs-lookup"><span data-stu-id="9f36f-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="9f36f-113">Se trata de la tabla de jerarquías integrada que se expone al cliente.</span><span class="sxs-lookup"><span data-stu-id="9f36f-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="9f36f-114">MAPI impone pocos requisitos en los escritores del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9f36f-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="9f36f-115">El intervalo de características posibles que puede implementar como un escritor de la libreta de direcciones es muy flexible y variado.</span><span class="sxs-lookup"><span data-stu-id="9f36f-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="9f36f-116">Por ejemplo, el proveedor puede limitarse a proporcionar una vista de solo lectura de un tipo concreto de información de destinatarios o implementar un conjunto completo de características, lo que permite a los clientes o a los proveedores realizar adiciones o modificaciones a los datos del destinatario y imponer Criterios de búsqueda para definir vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9f36f-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="9f36f-117">Los datos de su proveedor pueden residir localmente en un archivo o base de datos o en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="9f36f-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="9f36f-118">Algunos proveedores de libretas de direcciones están diseñados para funcionar con un sistema de mensajería determinado, estrechamente acoplados con un proveedor de transporte, mientras que otros pueden operar con cualquier sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9f36f-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="9f36f-119">MAPI define un tipo especial de proveedor de libreta de direcciones denominado libreta personal de direcciones, o PAB, que implementa un solo contenedor modificable y puede almacenar la información de destinatarios copiada de otros contenedores, así como la información que se crea directamente.</span><span class="sxs-lookup"><span data-stu-id="9f36f-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="9f36f-120">Aunque cualquier proveedor de libreta de direcciones puede implementar una PAB y varios PAB pueden agregarse a un perfil, solo se puede designar a uno de estos proveedores para que opere como PAB durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="9f36f-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

