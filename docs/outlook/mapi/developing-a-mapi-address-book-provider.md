---
title: Desarrollo de un proveedor de libreta de direcciones MAPI
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
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="5685a-103">Desarrollo de un proveedor de libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="5685a-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="5685a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5685a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5685a-105">Un proveedor de libreta de direcciones proporciona información de destinatarios a las aplicaciones cliente, al almacén de mensajes y a los proveedores de transporte y a MAPI.</span><span class="sxs-lookup"><span data-stu-id="5685a-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="5685a-106">La información del destinatario se organiza jerárquicamente en los compartimentos de almacenamiento conocidos como contenedores.</span><span class="sxs-lookup"><span data-stu-id="5685a-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="5685a-107">Cada libreta de direcciones del perfil contribuye con uno o más contenedores de nivel superior o primario a la libreta de direcciones MAPI, una vista integrada de la información de destinatarios de todos los proveedores de libretas de direcciones de una sesión.</span><span class="sxs-lookup"><span data-stu-id="5685a-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="5685a-108">Es a través de la libreta de direcciones MAPI que los clientes y otros proveedores de servicios obtienen acceso a los datos de un proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5685a-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="5685a-109">MAPI compila la libreta de direcciones integrada mediante:</span><span class="sxs-lookup"><span data-stu-id="5685a-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="5685a-110">Recuperación de los contenedores de nivel superior de cada proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5685a-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="5685a-111">Recuperación de la tabla de jerarquía de cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="5685a-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="5685a-112">Copiar cada tabla de jerarquía en una tabla de jerarquía integrada.</span><span class="sxs-lookup"><span data-stu-id="5685a-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="5685a-113">Es la tabla de jerarquía integrada que se expone al cliente.</span><span class="sxs-lookup"><span data-stu-id="5685a-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="5685a-114">MAPI impone pocos requisitos a los escritores de proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5685a-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="5685a-115">El rango de características posibles que puede implementar como escritor de libreta de direcciones es variado y flexible.</span><span class="sxs-lookup"><span data-stu-id="5685a-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="5685a-116">Por ejemplo, su proveedor podría limitarse a proporcionar una vista de solo lectura de un tipo determinado de información de destinatarios o implementar un conjunto completo de características, lo que tal vez permita a los clientes o proveedores realizar adiciones o modificaciones en los datos del destinatario e imponer criterios de búsqueda para definir vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5685a-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="5685a-117">Los datos del proveedor pueden residir localmente en un archivo o base de datos o en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5685a-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="5685a-118">Algunos proveedores de libreta de direcciones están diseñados para trabajar con un sistema de mensajería determinado, estrechamente unido a un proveedor de transporte, mientras que otros pueden operar con cualquier sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5685a-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="5685a-119">MAPI define un tipo especial de proveedor de libreta de direcciones denominado libreta de direcciones personal, o PAB, que implementa un único contenedor modificable y puede contener información de destinatarios copiada de otros contenedores, así como información creada directamente.</span><span class="sxs-lookup"><span data-stu-id="5685a-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="5685a-120">Aunque cualquier proveedor de libreta de direcciones puede implementar un PAB y varios PAB se pueden agregar a un perfil, solo uno de estos proveedores puede ser designado para funcionar como PAB durante cualquier sesión.</span><span class="sxs-lookup"><span data-stu-id="5685a-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

