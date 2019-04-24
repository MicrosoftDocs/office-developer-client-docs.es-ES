---
title: Mostrar hojas de propiedades de configuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316404"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="5b7e5-103">Mostrar hojas de propiedades de configuración</span><span class="sxs-lookup"><span data-stu-id="5b7e5-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="5b7e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b7e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b7e5-105">Los proveedores de transporte usan el método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para implementar las hojas de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="5b7e5-106">Cuando se llama a **DoConfigPropSheet**, el proveedor de transporte pasa un puntero a una matriz de propiedades junto con información sobre cómo mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="5b7e5-107">MAPI a continuación presenta las propiedades al usuario por medio de un cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="5b7e5-108">Se recomienda encarecidamente usar este mecanismo de hoja de propiedades al implementar el proveedor de transporte debido a las ventajas que tiene el usuario de una interfaz coherente.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="5b7e5-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="5b7e5-109">Transport providers</span></span>

<span data-ttu-id="5b7e5-110">Los proveedores de transporte pueden usar la función [BuildDisplayTable](builddisplaytable.md) para simplificar la creación de una tabla de presentación para su uso con **DoConfigPropSheet**.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="5b7e5-111">Los proveedores de transporte también pueden usar la API de la hoja de propiedades directamente.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="5b7e5-112">Para almacenar en búfer los cambios en las propiedades, los proveedores de transporte pueden usar la función [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="5b7e5-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="5b7e5-113">Esto simplifica el tratamiento de las cancelaciones por parte del usuario mientras el usuario modifica los valores almacenados en las propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="5b7e5-114">Si es necesario, un proveedor de transporte también puede proporcionar un cuadro de diálogo de Asistente para simplificar las tareas de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b7e5-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

