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
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816662"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="3570c-103">Desarrollar un proveedor de libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="3570c-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="3570c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3570c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3570c-105">Un proveedor de la libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, al almacén de mensajes y de los proveedores, de transporte y a MAPI.</span><span class="sxs-lookup"><span data-stu-id="3570c-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="3570c-106">Información de destinatarios se organiza jerárquicamente en compartimentos de almacenamiento conocidos como contenedores.</span><span class="sxs-lookup"><span data-stu-id="3570c-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="3570c-107">Cada libreta de direcciones en el perfil de contribuye a uno o más nivel superior, o primario, los contenedores de la libreta de direcciones MAPI, una vista integrada de información de todas las direcciones de los destinatarios book proveedores en una sesión.</span><span class="sxs-lookup"><span data-stu-id="3570c-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="3570c-108">Es a través de la libreta de direcciones MAPI que los clientes y otros proveedores de servicios de tener acceso a los datos de un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3570c-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="3570c-109">MAPI basa la libreta de direcciones integrada por:</span><span class="sxs-lookup"><span data-stu-id="3570c-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="3570c-110">Recuperación de los contenedores de nivel superior de cada proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3570c-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="3570c-111">Recuperación de tabla de jerarquía de cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="3570c-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="3570c-112">Copiar cada tabla de jerarquía en una tabla de jerarquías integrada.</span><span class="sxs-lookup"><span data-stu-id="3570c-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="3570c-113">Es la tabla de jerarquía integrada que se expone al cliente.</span><span class="sxs-lookup"><span data-stu-id="3570c-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="3570c-114">MAPI impone algunos requisitos en los escritores de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3570c-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="3570c-115">El intervalo de posibles características se puede implementar como un sistema de escritura de la libreta de direcciones es variado y flexible.</span><span class="sxs-lookup"><span data-stu-id="3570c-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="3570c-116">Por ejemplo, podría estar limitada a proporcionar una vista de solo lectura de un tipo determinado de información del destinatario o implementar un conjunto completo de características, quizás lo que permite los clientes o proveedores para realizar adiciones o modificaciones realizadas en los datos de destinatario y para imponer su proveedor de criterios de búsqueda para definir vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3570c-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="3570c-117">Los datos de su proveedor pueden residir localmente en un archivo o una base de datos o en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3570c-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="3570c-118">Algunos proveedores de libreta de direcciones están diseñados para trabajar con un sistema de mensajería determinado, estrechamente con un proveedor de transporte, mientras que otros usuarios pueden funcionar con cualquier sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3570c-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="3570c-119">MAPI define un tipo especial de proveedor de libreta de direcciones que llama a una libreta de direcciones personales o PAB, que implementa un único contenedor modificable y puede contener información de destinatarios copió desde otros contenedores, así como información creada directamente.</span><span class="sxs-lookup"><span data-stu-id="3570c-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="3570c-120">Aunque cualquier proveedor de la libreta de direcciones puede implementar una PAB y varios PAB puede agregarse a un perfil, se puede designar sólo uno de estos proveedores para funcionar como el archivo PAB durante una sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="3570c-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

