---
title: XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'El elemento Capabilities del esquema XML del proveedor (OSC) permite a un proveedor OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356451"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="7809f-104">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="7809f-104">XML for capabilities</span></span>

<span data-ttu-id="7809f-105">El elemento **Capabilities** del esquema XML del proveedor (OSC) permite a un proveedor OSC especificar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7809f-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="7809f-106">Esta funcionalidad incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7809f-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="7809f-107">Si el proveedor admite la obtención, el almacenamiento en caché o la búsqueda dinámica de amigos y actividades desde la red social.</span><span class="sxs-lookup"><span data-stu-id="7809f-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="7809f-108">Cómo el OSC debe mostrar ciertas interfaces de inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="7809f-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="7809f-109">Si OSC debe usar la autenticación basada en formularios o configurar automáticamente la red social e iniciar sesión en el usuario en la red social.</span><span class="sxs-lookup"><span data-stu-id="7809f-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="7809f-110">El esquema XML para **capacidades** es crítico porque identifica a la funcionalidad admitida por el proveedor para el OSC.</span><span class="sxs-lookup"><span data-stu-id="7809f-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="7809f-111">Un proveedor OSC debe implementar el método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) que devuelve una cadena de _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="7809f-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="7809f-112">El OSC llama a **ISocialProvider:: GetCapabilities** para obtener información sobre las funciones del proveedor OSC en la cadena de _resultado_ , que cumple con la definición del esquema XML para el elemento **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="7809f-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="7809f-113">Esta información permite que las llamadas posteriores desde el OSC al proveedor de OSC funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="7809f-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="7809f-114">Para especificar las capacidades de un proveedor de OSC como un parámetro de salida del método **ISocialProvider:: GetCapabilities** , debe cumplir con el esquema XML de extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="7809f-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="7809f-115">En la siguiente figura se muestra la estructura XML **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="7809f-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="7809f-116">**Figura 1. \<estructura\> XML de capacidades**</span><span class="sxs-lookup"><span data-stu-id="7809f-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Estructura XML de capacidades](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="7809f-118">Para obtener descripciones detalladas de los elementos secundarios del elemento **Capabilities** , vea [Capabilities XML Elements](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="7809f-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="7809f-119">Para obtener un ejemplo de XML de **capacidades** , vea el [ejemplo de XML de Capabilities](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="7809f-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="7809f-120">Para obtener una definición completa del esquema XML del proveedor de OSC, incluidos los elementos necesarios u opcionales, vea el [esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="7809f-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7809f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7809f-121">See also</span></span>

- [<span data-ttu-id="7809f-122">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="7809f-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="7809f-123">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="7809f-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="7809f-124">XML para amigos</span><span class="sxs-lookup"><span data-stu-id="7809f-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="7809f-125">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="7809f-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="7809f-126">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="7809f-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

