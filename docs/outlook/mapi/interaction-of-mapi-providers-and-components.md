---
title: Interacción de componentes y proveedores MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592629"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="4cbae-103">Interacción de componentes y proveedores MAPI</span><span class="sxs-lookup"><span data-stu-id="4cbae-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="4cbae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cbae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cbae-105">Proveedores de servicios de MAPI de ningún tipo deben seguir ciertas instrucciones para trabajar con otros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cbae-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="4cbae-106">Cada proveedor de servicios debe:</span><span class="sxs-lookup"><span data-stu-id="4cbae-106">Each service provider must:</span></span>
  
- <span data-ttu-id="4cbae-107">Usar los objetos de proveedor y el inicio de sesión correctos para la inicialización.</span><span class="sxs-lookup"><span data-stu-id="4cbae-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="4cbae-108">Devolver una tabla de distribución de proveedor de puntos de entrada para el sistema de mensajería en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="4cbae-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="4cbae-109">Registrar una fila de tabla de estado MAPI para cada recurso propiedad por el proveedor y llame al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) en los momentos adecuados.</span><span class="sxs-lookup"><span data-stu-id="4cbae-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="4cbae-110">Use el método [IMAPISupport::NewUID](imapisupport-newuid.md) para obtener los identificadores exclusivos válidos (UID).</span><span class="sxs-lookup"><span data-stu-id="4cbae-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="4cbae-111">Admite las interfaces MAPI comunes en los objetos que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="4cbae-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="4cbae-112">Use las funciones de asignación de memoria MAPI para asignar la memoria que se devuelven a las aplicaciones de cliente y para liberar memoria asignada por otros elementos del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cbae-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="4cbae-113">Mantener una sección de perfil, si es necesario, para almacenar las credenciales para el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="4cbae-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="4cbae-114">Utilice el método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar los mensajes de las funciones de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="4cbae-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="4cbae-115">Incluyen los archivos de encabezado adecuado (incluido mapispi.h) que definición constantes comunes, estructuras, interfaces y valores devuelven.</span><span class="sxs-lookup"><span data-stu-id="4cbae-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="4cbae-116">Siga las convenciones de formato de dirección para los tipos de dirección comunes.</span><span class="sxs-lookup"><span data-stu-id="4cbae-116">Follow address format conventions for common address types.</span></span>
    

