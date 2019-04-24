---
title: Inicio de una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336347"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="77753-103">Inicio de una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="77753-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="77753-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77753-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77753-105">Aunque hay una cantidad significativa de trabajo durante el inicio de la sesión, las tareas necesarias son mínimas.</span><span class="sxs-lookup"><span data-stu-id="77753-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="77753-106">Gran parte de este trabajo se realiza en el procesamiento de MAPI de las llamadas de [MAPIInitialize](mapiinitialize.md) y [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="77753-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="77753-107">Estas dos funciones aceptan marcas como parámetros de entrada para controlar aspectos de la sesión, como el control de notificaciones y la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="77753-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="77753-108">Es importante comprender las consecuencias de establecer cada una de estas marcas al llamar a **MAPIInitialize** para inicializar las bibliotecas MAPI y **MAPILogonEx** para iniciar sesión en el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="77753-109">**Para iniciar una sesión MAPI**</span><span class="sxs-lookup"><span data-stu-id="77753-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="77753-110">Llame a **MAPIInitialize** para inicializar el conjunto estándar de bibliotecas MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="77753-111">Si necesita usar las bibliotecas OLE, llame a la función OLE [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="77753-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="77753-112">Si necesita usar la biblioteca de utilidades MAPI, llame a [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="77753-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="77753-113">Llame a **MAPILogonEx** con un perfil válido para iniciar sesión en el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="77753-114">**MAPILogonEx** comprueba la configuración de cada uno de los proveedores de servicios en los servicios de mensajes incluidos en el perfil, solicitando al usuario información adicional si es necesario y es posible.</span><span class="sxs-lookup"><span data-stu-id="77753-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="77753-115">Cuando se completa **MAPILogonEx** , los proveedores de servicios configurados están listos para el servicio.</span><span class="sxs-lookup"><span data-stu-id="77753-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="77753-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="77753-116">In this section</span></span>

[<span data-ttu-id="77753-117">Inicializar MAPI</span><span class="sxs-lookup"><span data-stu-id="77753-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="77753-118">Describe cómo inicializar MAPI para una sesión.</span><span class="sxs-lookup"><span data-stu-id="77753-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="77753-119">Inicializar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="77753-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="77753-120">Describe las llamadas que se realizan para inicializar OLE para su uso con MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="77753-121">Inicializar las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="77753-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="77753-122">Describe cómo inicializar las herramientas MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="77753-123">Iniciar sesión en MAPI</span><span class="sxs-lookup"><span data-stu-id="77753-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="77753-124">Describe cómo las aplicaciones cliente inician sesión en el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="77753-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

