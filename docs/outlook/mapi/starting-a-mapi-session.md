---
title: Iniciar una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820754"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="ee841-103">Iniciar una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="ee841-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="ee841-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee841-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee841-105">Aunque hay una gran cantidad de trabajo realizado durante la sesión de inicio, las tareas necesarias son mínimas.</span><span class="sxs-lookup"><span data-stu-id="ee841-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="ee841-106">Gran parte de este trabajo se realiza en la MAPI de procesamiento de las llamadas [MAPIInitialize](mapiinitialize.md) y [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="ee841-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="ee841-107">Ambas funciones aceptan marcas como parámetros de entrada para controlar aspectos de la sesión, como control de notificación y la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ee841-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="ee841-108">Es importante comprender las consecuencias de la configuración de cada uno de estos marcadores al llamar a **MAPIInitialize** para inicializar las bibliotecas de MAPI y **MAPILogonEx** para iniciar sesión en el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="ee841-109">**Para iniciar una sesión MAPI**</span><span class="sxs-lookup"><span data-stu-id="ee841-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="ee841-110">Llamar a **MAPIInitialize** para inicializar el conjunto estándar de las bibliotecas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="ee841-111">Si necesita usar las bibliotecas de OLE, llame a la función OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee841-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="ee841-112">Si necesita usar la biblioteca de utilidades MAPI, llame a [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="ee841-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="ee841-113">Llame al método **MAPILogonEx** con un perfil válido para iniciar sesión en el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="ee841-114">**MAPILogonEx** comprueba la configuración de cada uno de los proveedores de servicios en los servicios de mensaje incluidos en el perfil, preguntar al usuario para obtener información adicional, si es necesario y posibles.</span><span class="sxs-lookup"><span data-stu-id="ee841-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="ee841-115">Una vez completada **MAPILogonEx** , están listos para el servicio de los proveedores de servicio configurado.</span><span class="sxs-lookup"><span data-stu-id="ee841-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="ee841-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ee841-116">In this section</span></span>

[<span data-ttu-id="ee841-117">Inicializar MAPI</span><span class="sxs-lookup"><span data-stu-id="ee841-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="ee841-118">Describe cómo inicializar MAPI para una sesión.</span><span class="sxs-lookup"><span data-stu-id="ee841-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="ee841-119">Inicializar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="ee841-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="ee841-120">Describe las llamadas para realizar en inicializar OLE para su uso con MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="ee841-121">Inicializar las herramientas MAPI</span><span class="sxs-lookup"><span data-stu-id="ee841-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="ee841-122">Describe cómo inicializar utilidades MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="ee841-123">Iniciar sesión en MAPI</span><span class="sxs-lookup"><span data-stu-id="ee841-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="ee841-124">Describe cómo las aplicaciones cliente inicie sesión en el sistema de sub MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee841-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

