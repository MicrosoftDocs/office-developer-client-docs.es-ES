---
title: Funciones no compatibles con los administradores de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816502"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="8bd22-103">Funciones no compatibles con los administradores de formulario</span><span class="sxs-lookup"><span data-stu-id="8bd22-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="8bd22-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8bd22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8bd22-105">Las siguientes características no son compatibles con el Administrador de formulario predeterminado por motivos de rendimiento, pero pueden ser compatibles con los administradores de formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="8bd22-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="8bd22-106">Una jerarquía que permite formularios se agrupan o clasifican a lo largo de una biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="8bd22-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="8bd22-107">Una biblioteca de formularios es una base de datos de archivos planos de formularios.</span><span class="sxs-lookup"><span data-stu-id="8bd22-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="8bd22-108">Control de acceso para las categorías de formularios, correspondiente a las clases de mensajes o superclase.</span><span class="sxs-lookup"><span data-stu-id="8bd22-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="8bd22-109">Compatibilidad con varias versiones de idioma del mismo formulario en una biblioteca de formularios único.</span><span class="sxs-lookup"><span data-stu-id="8bd22-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="8bd22-110">Estos son los problemas de implementación.</span><span class="sxs-lookup"><span data-stu-id="8bd22-110">These are implementation issues.</span></span> <span data-ttu-id="8bd22-111">No hay nada para evitar que el Administrador de un formulario personalizado de la implementación de estas características.</span><span class="sxs-lookup"><span data-stu-id="8bd22-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="8bd22-112">La arquitectura de formulario MAPI no admite la ejecución simultánea de varios directores de formulario.</span><span class="sxs-lookup"><span data-stu-id="8bd22-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="8bd22-113">Aunque MAPI admite varios proveedores de almacén de mensajes de usuarios simultáneos, los proveedores de transporte y los proveedores de la libreta de direcciones, se admite solo un administrador de formulario simple.</span><span class="sxs-lookup"><span data-stu-id="8bd22-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="8bd22-114">Debido a que el formulario sólo un administrador puede estar en ejecución a la vez, si implementa el Administrador de un formulario personalizado debe volver a implementar cualquier funcionalidad desde el Administrador de formulario predeterminado que necesita.</span><span class="sxs-lookup"><span data-stu-id="8bd22-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="8bd22-115">Debido a que el Administrador de su formulario personalizado reemplazará por completo el Administrador de forma predeterminada, las funciones del Administrador de formulario predeterminado de no estará disponibles a menos que se duplican en el Administrador de su formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="8bd22-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8bd22-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="8bd22-116">See also</span></span>



[<span data-ttu-id="8bd22-117">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="8bd22-117">MAPI Forms</span></span>](mapi-forms.md)

