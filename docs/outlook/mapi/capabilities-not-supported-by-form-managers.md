---
title: Funcionalidades no admitidas por los administradores de formularios
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
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="f7f9f-103">Funcionalidades no admitidas por los administradores de formularios</span><span class="sxs-lookup"><span data-stu-id="f7f9f-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="f7f9f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7f9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7f9f-105">El administrador de formularios predeterminado no admite las siguientes características por motivos de rendimiento, pero pueden ser compatibles con administradores de formularios personalizados.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="f7f9f-106">Jerarquía que permite agrupar o clasificar formularios en una biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="f7f9f-107">Una biblioteca de formularios es una base de datos de archivos planos de formularios.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="f7f9f-108">Control de acceso para categorías de formularios, correspondientes a clases de mensaje o superclases.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="f7f9f-109">Compatibilidad con varias versiones de idioma del mismo formulario en una sola biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="f7f9f-110">Estos son problemas de implementación.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-110">These are implementation issues.</span></span> <span data-ttu-id="f7f9f-111">No hay nada que impida que un administrador de formularios personalizado implemente estas características.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="f7f9f-112">La arquitectura de formulario MAPI no admite varios administradores de formularios que se ejecutan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="f7f9f-113">Aunque MAPI admite varios proveedores de almacén de mensajes simultáneos, proveedores de transporte y proveedores de libreta de direcciones, solo se admite un administrador de formularios único.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="f7f9f-114">Dado que solo se puede ejecutar un administrador de formularios a la vez, si implementa un administrador de formularios personalizado, tendrá que volver a implementar cualquier funcionalidad del administrador de formularios predeterminado que necesite.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="f7f9f-115">Dado que el administrador de formularios personalizado reemplazará por completo al administrador de formularios predeterminado, las capacidades del administrador de formularios predeterminado no estarán disponibles a menos que se dupliquen en el administrador de formularios personalizado.</span><span class="sxs-lookup"><span data-stu-id="f7f9f-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7f9f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7f9f-116">See also</span></span>



[<span data-ttu-id="f7f9f-117">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="f7f9f-117">MAPI Forms</span></span>](mapi-forms.md)

