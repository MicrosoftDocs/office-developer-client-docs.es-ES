---
title: Prepararse para publicar un proveedor de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugieren pruebas que puede realizar antes de lanzar el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414665"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="d72ce-103">Prepararse para publicar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="d72ce-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="d72ce-104">En esta sección se sugieren pruebas que puede realizar antes de lanzar el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d72ce-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="d72ce-105">Puedes empezar a hacer referencia a los temas de esta sección y llevar a cabo algunas de estas pruebas durante las fases de desarrollo y pruebas, pero debes haber completado estas pruebas en el momento de publicar.</span><span class="sxs-lookup"><span data-stu-id="d72ce-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="d72ce-106">Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces del proveedor de OSC con respecto a las funcionalidades que especifique para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="d72ce-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="d72ce-107">Además, aunque el OSC es una característica compartida por varias aplicaciones cliente de Office, estas pruebas usan Outlook como cliente para probar la funcionalidad fundamental.</span><span class="sxs-lookup"><span data-stu-id="d72ce-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="d72ce-108">Debe determinar si son necesarias otras pruebas para características específicas de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="d72ce-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d72ce-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d72ce-109">In this section</span></span>

- <span data-ttu-id="d72ce-110">[Implementación de](testing-deployment.md)pruebas: describe los escenarios que debes probar en torno a la instalación y desinstalación de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="d72ce-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="d72ce-111">[Capacidades de prueba, autenticación](testing-capabilities-authentication-and-configuration.md)y configuración: describe las pruebas para obtener funcionalidades y escenarios en torno a la configuración de una cuenta y la autenticación de un usuario para una red social.</span><span class="sxs-lookup"><span data-stu-id="d72ce-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="d72ce-112">[Pruebas siguientes y Stop-Following personas:](testing-following-and-stop-following-persons.md)describe escenarios para probar la capacidad del proveedor de OSC para agregar a una persona como un amigo o para quitar a un amigo de la red social.</span><span class="sxs-lookup"><span data-stu-id="d72ce-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="d72ce-113">[Pruebas](testing-friends.md)de amigos: describe pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente datos de amigos y no amigos, si procede, según el modo de sincronización que admita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d72ce-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="d72ce-114">[Actividades](testing-activities.md)de prueba: describe pruebas y escenarios para comprobar que el proveedor de OSC devuelve correctamente las actividades de amigos y no amigos, si procede, según el modo de sincronización que admita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d72ce-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="d72ce-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="d72ce-115">Reference</span></span>

- [<span data-ttu-id="d72ce-116">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d72ce-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="d72ce-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="d72ce-117">Related sections</span></span>

- [<span data-ttu-id="d72ce-118">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="d72ce-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="d72ce-119">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="d72ce-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="d72ce-120">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="d72ce-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="d72ce-121">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="d72ce-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="d72ce-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="d72ce-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

