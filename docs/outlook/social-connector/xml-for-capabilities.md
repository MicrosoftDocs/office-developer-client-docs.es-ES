---
title: XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'El elemento de funciones en el esquema XML de proveedor (OSC) permite que un proveedor de OSC especificar su funcionalidad. Esta funcionalidad incluye lo siguiente:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821215"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="d5a2b-104">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="d5a2b-104">XML for capabilities</span></span>

<span data-ttu-id="d5a2b-105">El elemento de **funciones** en el esquema XML de proveedor (OSC) permite que un proveedor de OSC especificar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="d5a2b-106">Esta funcionalidad incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5a2b-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="d5a2b-107">Si el proveedor admite la introducción, el almacenamiento en caché o buscar dinámicamente amigos y actividades de la red social.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="d5a2b-108">Cómo el OSC debe mostrar ciertas interfaces de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="d5a2b-109">Si el OSC debe usar la autenticación basada en formularios o configurar automáticamente las redes sociales y los registros en el usuario en la red social.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="d5a2b-110">El esquema XML de **las capacidades** es fundamental ya que identifica a la OSC la funcionalidad admitida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="d5a2b-111">Un proveedor de OSC debe implementar el método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que devuelve una cadena de _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="d5a2b-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="d5a2b-112">El OSC llama a **ISocialProvider::GetCapabilities** para obtener información acerca de las capacidades del proveedor de OSC en la cadena de _resultado_ , que cumple con la definición del esquema XML para el elemento **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d5a2b-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="d5a2b-113">Esta información permite las llamadas posteriores desde el OSC para el proveedor de OSC funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="d5a2b-114">Para especificar las capacidades de un proveedor de OSC como un parámetro de salida del método **ISocialProvider::GetCapabilities** , debe cumplir el esquema XML de extensibilidad de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="d5a2b-115">La siguiente ilustración muestra la estructura XML de **las capacidades** .</span><span class="sxs-lookup"><span data-stu-id="d5a2b-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="d5a2b-116">**En la figura 1. \<capacidades\> estructura XML**</span><span class="sxs-lookup"><span data-stu-id="d5a2b-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![Estructura XML de capacidades](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="d5a2b-118">Para obtener descripciones detalladas de los elementos secundarios del elemento de **funciones** , vea [Los elementos XML de las capacidades](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="d5a2b-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="d5a2b-119">Para obtener un ejemplo de XML de las **capacidades** , vea [Ejemplo de XML de las capacidades](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="d5a2b-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="d5a2b-120">Para ver una definición completa del esquema XML de proveedor OSC, incluido qué elementos son obligatorios u opcionales, vea [Esquema de XML de Outlook Social Connector proveedor](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d5a2b-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5a2b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5a2b-121">See also</span></span>

- [<span data-ttu-id="d5a2b-122">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="d5a2b-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="d5a2b-123">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="d5a2b-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="d5a2b-124">XML de amigos</span><span class="sxs-lookup"><span data-stu-id="d5a2b-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="d5a2b-125">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="d5a2b-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="d5a2b-126">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="d5a2b-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

