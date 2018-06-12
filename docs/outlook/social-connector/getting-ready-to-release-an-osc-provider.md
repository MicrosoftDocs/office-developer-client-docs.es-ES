---
title: Prepararse liberar un proveedor de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugiere las pruebas que se puede hacer antes de liberar su proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821092"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="dfe89-103">Prepararse liberar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="dfe89-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="dfe89-104">En esta sección se sugiere las pruebas que se puede hacer antes de liberar su proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="dfe89-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="dfe89-105">Puede iniciar con respecto a los temas de esta sección y realizar algunas de estas pruebas durante el desarrollo y las fases de pruebas, pero debe haber completado estas pruebas en el momento en que se suelte.</span><span class="sxs-lookup"><span data-stu-id="dfe89-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="dfe89-106">Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces de proveedor OSC con respecto a las capacidades que especifique para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="dfe89-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="dfe89-107">Además, aunque el OSC es una característica compartida por varias aplicaciones de cliente de Office, estas pruebas utilizan Outlook como el cliente para probar la funcionalidad fundamental.</span><span class="sxs-lookup"><span data-stu-id="dfe89-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="dfe89-108">Debe determinar si otras pruebas son necesarias para características específicas a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="dfe89-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="dfe89-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dfe89-109">In this section</span></span>

- <span data-ttu-id="dfe89-110">[Pruebas de implementación](testing-deployment.md): describe escenarios en los que se debe probar a la instalación y desinstalación de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="dfe89-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="dfe89-111">[Capacidades de las pruebas, la autenticación y la configuración](testing-capabilities-authentication-and-configuration.md): describe las pruebas de introducción, características y escenarios de configuración de una cuenta y la autenticación de un usuario para una red social.</span><span class="sxs-lookup"><span data-stu-id="dfe89-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="dfe89-112">[Las pruebas siguientes y las personas o deje de seguir](testing-following-and-stop-following-persons.md): se describen escenarios para comprobar la capacidad de un proveedor OSC para agregar una persona como un amigo, o para quitar un amigo desde la red social.</span><span class="sxs-lookup"><span data-stu-id="dfe89-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="dfe89-113">[Prueba de amigos](testing-friends.md): describe las pruebas y escenarios para comprobar que el proveedor de OSC adecuadamente devuelve datos de amigos y que no sean-amigos, en su caso, según el modo de sincronización que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="dfe89-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="dfe89-114">[Las actividades de pruebas](testing-activities.md): describe las pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente las actividades de amigos y que no sean-amigos, en su caso, según el modo de sincronización que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="dfe89-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="dfe89-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="dfe89-115">Reference</span></span>

- [<span data-ttu-id="dfe89-116">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="dfe89-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="dfe89-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="dfe89-117">Related sections</span></span>

- [<span data-ttu-id="dfe89-118">Plantillas de ejemplo OSC</span><span class="sxs-lookup"><span data-stu-id="dfe89-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="dfe89-119">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="dfe89-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="dfe89-120">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="dfe89-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="dfe89-121">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="dfe89-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="dfe89-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="dfe89-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

