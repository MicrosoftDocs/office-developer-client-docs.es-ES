---
title: Introducción al proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433160"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="bfd6e-103">Introducción al proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="bfd6e-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="bfd6e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfd6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfd6e-105">Un proveedor de transporte es una biblioteca de vínculos dinámicos (DLL) que actúa como intermediario entre el subsistema MAPI y uno o varios sistemas de mensajería subyacentes.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="bfd6e-106">Un sistema de mensajería es un mecanismo específico por el que se envían y reciben mensajes.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="bfd6e-107">Algunos ejemplos de sistemas de mensajería son:</span><span class="sxs-lookup"><span data-stu-id="bfd6e-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="bfd6e-108">Un sistema de archivos de red compartido en el que el proveedor de transporte escribe mensajes directamente.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="bfd6e-109">Una interfaz de red TCP/IP que el proveedor de transporte usa para conectarse a un servidor de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="bfd6e-110">Un servicio en línea al que los usuarios se conectan.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="bfd6e-111">Un sistema de automatización de office o mensajería basada en host.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="bfd6e-112">Un conjunto de llamadas de procedimiento remoto a un servidor de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="bfd6e-113">Cualquier cosa que se pueda usar para transferir datos de un equipo a otro.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="bfd6e-114">Un DLL del proveedor de transporte debe cumplir con la interfaz especificada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="bfd6e-115">Como desarrollador del proveedor de transporte, implementará esta interfaz en términos de la funcionalidad presente en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bfd6e-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

