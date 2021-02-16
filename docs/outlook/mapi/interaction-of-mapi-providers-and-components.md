---
title: Interacción de los proveedores y componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434665"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="b6101-103">Interacción de los proveedores y componentes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6101-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="b6101-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6101-105">Los proveedores de servicios MAPI de cualquier tipo deben seguir determinadas directrices para trabajar con otros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6101-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="b6101-106">Cada proveedor de servicios debe:</span><span class="sxs-lookup"><span data-stu-id="b6101-106">Each service provider must:</span></span>
  
- <span data-ttu-id="b6101-107">Use el proveedor adecuado y los objetos de inicio de sesión para inicialización.</span><span class="sxs-lookup"><span data-stu-id="b6101-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="b6101-108">Devolver una tabla de envío de puntos de entrada del proveedor al sistema de mensajería tras la inicialización.</span><span class="sxs-lookup"><span data-stu-id="b6101-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="b6101-109">Registre una fila de tabla de estado MAPI para cada recurso que sea propiedad del proveedor y llame al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="b6101-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="b6101-110">Use el [método IMAPISupport::NewUID](imapisupport-newuid.md) para obtener identificadores únicos válidos (UID).</span><span class="sxs-lookup"><span data-stu-id="b6101-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="b6101-111">Admite las interfaces MAPI comunes en los objetos que devuelve.</span><span class="sxs-lookup"><span data-stu-id="b6101-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="b6101-112">Use las funciones de asignación de memoria MAPI para asignar la memoria devuelta a las aplicaciones cliente y liberar memoria asignada por otras partes del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6101-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="b6101-113">Mantenga una sección de perfil, si es necesario, para almacenar las credenciales en el sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="b6101-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="b6101-114">Use el [método IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar las funciones de preprocesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b6101-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="b6101-115">Incluya los archivos de encabezado adecuados (incluido mapispi.h) que definen constantes comunes, estructuras, interfaces y valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="b6101-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="b6101-116">Siga las convenciones de formato de dirección para tipos de direcciones comunes.</span><span class="sxs-lookup"><span data-stu-id="b6101-116">Follow address format conventions for common address types.</span></span>
    

