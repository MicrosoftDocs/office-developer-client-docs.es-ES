---
title: Mostrar las hojas de propiedades de configuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aa3ddecbd5af56eef16f5ae3a349a027e689fc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816693"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="ed49f-103">Mostrar las hojas de propiedades de configuración</span><span class="sxs-lookup"><span data-stu-id="ed49f-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="ed49f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed49f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed49f-105">Proveedores de transporte de utilizar el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para implementar las hojas de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="ed49f-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="ed49f-106">Cuando se llama a **DoConfigPropSheet**, el proveedor de transporte pasa un puntero a una matriz de propiedades junto con información sobre cómo mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="ed49f-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="ed49f-107">MAPI, a continuación, presenta las propiedades al usuario por medio de un cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="ed49f-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="ed49f-108">Se recomienda encarecidamente usar este mecanismo de hoja de propiedad al implementar el proveedor de transporte debido a la ventaja para el usuario de una interfaz coherente.</span><span class="sxs-lookup"><span data-stu-id="ed49f-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="ed49f-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="ed49f-109">Transport providers</span></span>

<span data-ttu-id="ed49f-110">Los proveedores de transporte pueden usar la función [BuildDisplayTable](builddisplaytable.md) para simplificar la creación de una tabla para mostrar para su uso con **DoConfigPropSheet**.</span><span class="sxs-lookup"><span data-stu-id="ed49f-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="ed49f-111">Los proveedores de transporte también pueden usar la API de la hoja de propiedad directamente.</span><span class="sxs-lookup"><span data-stu-id="ed49f-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="ed49f-112">Tamaño de búfer de los cambios realizados en las propiedades, los proveedores de transporte, puede usar la función [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="ed49f-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="ed49f-113">Esto simplifica el control de cancelaciones por el usuario, mientras que el usuario modifica los valores almacenados en las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed49f-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="ed49f-114">Si es necesario, un proveedor de transporte también puede proporcionar un cuadro de diálogo Asistente para cuadro para simplificar las tareas de configuración para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ed49f-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

