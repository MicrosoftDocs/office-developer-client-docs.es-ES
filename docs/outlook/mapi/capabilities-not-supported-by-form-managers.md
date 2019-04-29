---
title: Capacidades no admitidas por los administradores de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419383"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="63255-103">Capacidades no admitidas por los administradores de formularios</span><span class="sxs-lookup"><span data-stu-id="63255-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="63255-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63255-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63255-105">Las siguientes características no son compatibles con el administrador de formularios predeterminado por motivos de rendimiento, pero pueden ser compatibles con los administradores de formularios personalizados.</span><span class="sxs-lookup"><span data-stu-id="63255-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="63255-106">Una jerarquía que permite agrupar o clasificar formularios en una biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="63255-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="63255-107">Una biblioteca de formularios es una base de datos de archivos sin formato de los formularios.</span><span class="sxs-lookup"><span data-stu-id="63255-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="63255-108">Control de acceso para categorías de formularios, correspondientes a las clases de mensaje o las superclases.</span><span class="sxs-lookup"><span data-stu-id="63255-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="63255-109">Compatibilidad con versiones de varios idiomas del mismo formulario en una única biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="63255-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="63255-110">Estos son problemas de implementación.</span><span class="sxs-lookup"><span data-stu-id="63255-110">These are implementation issues.</span></span> <span data-ttu-id="63255-111">No hay nada que impida que un administrador de formularios personalizado implemente estas características.</span><span class="sxs-lookup"><span data-stu-id="63255-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="63255-112">La arquitectura de formularios MAPI no es compatible con varios administradores de formularios que se ejecutan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="63255-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="63255-113">Aunque MAPI admite varios proveedores de almacenamiento de mensajes simultáneos, proveedores de transporte y proveedores de libretas de direcciones, solo se admite un único administrador de formularios.</span><span class="sxs-lookup"><span data-stu-id="63255-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="63255-114">Como solo se puede ejecutar un administrador de formularios a la vez, si implementa un administrador de formularios personalizado tendrá que volver a implementar cualquier funcionalidad del administrador de formularios predeterminado que necesite.</span><span class="sxs-lookup"><span data-stu-id="63255-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="63255-115">Como el administrador de formularios personalizado reemplazará por completo el administrador de formularios predeterminado, las capacidades del administrador de formularios predeterminado no estarán disponibles a menos que se dupliquen en el administrador de formularios personalizado.</span><span class="sxs-lookup"><span data-stu-id="63255-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63255-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="63255-116">See also</span></span>



[<span data-ttu-id="63255-117">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="63255-117">MAPI Forms</span></span>](mapi-forms.md)

