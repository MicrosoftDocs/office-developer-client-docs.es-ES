---
title: Almacenes de mensaje predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816625"
---
# <a name="default-message-stores"></a><span data-ttu-id="902a3-103">Almacenes de mensaje predeterminado</span><span class="sxs-lookup"><span data-stu-id="902a3-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="902a3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="902a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="902a3-p101">Un almac�n de mensajes predeterminado es aquel que las aplicaciones de cliente pueden utilizar para tareas de mensajer�a de prop�sito general. Hay una serie de caracter�sticas opcionales para los proveedores de almac�n de mensajes que pasan a ser necesarios si el proveedor de almac�n de mensajes es que se utilizar� como almac�n de mensajes predeterminado. Son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="902a3-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="902a3-108">Implementaci�n de las carpetas especiales: las carpetas Bandeja de entrada, Bandeja de salida y los resultados de b�squeda.</span><span class="sxs-lookup"><span data-stu-id="902a3-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="902a3-109">Proporcionar informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="902a3-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="902a3-110">Permitir env�os de mensajes entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="902a3-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="902a3-111">Permitir la creaci�n de mensajes con clases de mensaje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="902a3-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="902a3-112">Compatibilidad con las propiedades con nombre y varios valores.</span><span class="sxs-lookup"><span data-stu-id="902a3-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="902a3-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span><span class="sxs-lookup"><span data-stu-id="902a3-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="902a3-p102">Supporting associated contents tables. For more information, see [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="902a3-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="902a3-116">Compatibilidad con notificaci�n de la cola MAPI cuando hay mensajes en la cola de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="902a3-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="902a3-117">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="902a3-117">See also</span></span>



[<span data-ttu-id="902a3-118">Desarrollar un proveedor de almac�n de mensajes de MAPI</span><span class="sxs-lookup"><span data-stu-id="902a3-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

