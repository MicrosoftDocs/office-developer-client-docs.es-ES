---
title: Información general sobre el proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820897"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="39b7a-103">Información general sobre el proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="39b7a-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="39b7a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39b7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39b7a-105">Un proveedor de transporte es una biblioteca de vínculos dinámicos (DLL) que actúa como intermediario entre el subsistema MAPI y uno o varios sistemas de mensajería subyacentes.</span><span class="sxs-lookup"><span data-stu-id="39b7a-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="39b7a-106">Un sistema de mensajería es algunos mecanismo específico mediante el cual se envían y reciben los mensajes.</span><span class="sxs-lookup"><span data-stu-id="39b7a-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="39b7a-107">Algunos ejemplos de sistemas de mensajería son:</span><span class="sxs-lookup"><span data-stu-id="39b7a-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="39b7a-108">Un sistema de archivos de red compartida que el proveedor de transporte escribe los mensajes a directamente.</span><span class="sxs-lookup"><span data-stu-id="39b7a-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="39b7a-109">Una interfaz de red TCP/IP que usa el proveedor de transporte para conectarse a un servidor de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39b7a-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="39b7a-110">Un servicio en línea que los usuarios se conectan a.</span><span class="sxs-lookup"><span data-stu-id="39b7a-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="39b7a-111">Un host sistema basado en mensajería o office automatización.</span><span class="sxs-lookup"><span data-stu-id="39b7a-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="39b7a-112">Un conjunto de llamadas a procedimiento remoto a un servidor de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39b7a-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="39b7a-113">Cualquier cosa que se puede usar para transferir datos desde un equipo a otro.</span><span class="sxs-lookup"><span data-stu-id="39b7a-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="39b7a-114">Una DLL del proveedor de transporte debe cumplir con la interfaz especificada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="39b7a-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="39b7a-115">Como desarrollador de proveedor de transporte, se implementará esta interfaz en cuanto a la funcionalidad presente en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39b7a-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

