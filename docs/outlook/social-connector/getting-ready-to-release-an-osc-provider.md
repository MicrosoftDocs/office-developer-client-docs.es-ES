---
title: Preparación para la publicación de un proveedor OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: En esta sección se sugieren las pruebas que puede realizar antes de liberar su proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414665"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="1b4a4-103">Preparación para la publicación de un proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="1b4a4-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="1b4a4-104">En esta sección se sugieren las pruebas que puede realizar antes de liberar su proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="1b4a4-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="1b4a4-105">Puede empezar a hacer referencia a los temas de esta sección y realizar algunas de estas pruebas durante las fases de desarrollo y pruebas, pero debe haber completado estas pruebas en el momento de la publicación.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="1b4a4-106">Estas pruebas comprueban la funcionalidad básica de la implementación de las interfaces del proveedor de OSC con respecto a las capacidades especificadas para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="1b4a4-107">Además, aunque OSC es una característica compartida por varias aplicaciones cliente de Office, estas pruebas usan Outlook como cliente para probar la funcionalidad fundamental.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="1b4a4-108">Debe determinar si hay otras pruebas necesarias para las características específicas de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1b4a4-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1b4a4-109">In this section</span></span>

- <span data-ttu-id="1b4a4-110">[Prueba](testing-deployment.md)de la implementación: describe los escenarios que se deben probar en la instalación y desinstalación de un proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="1b4a4-111">[Capacidades de prueba, autenticación y configuración](testing-capabilities-authentication-and-configuration.md): describe las pruebas para obtener capacidades y los escenarios en los que se configura una cuenta y se autentica a un usuario para una red social.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="1b4a4-112">[Pruebas de seguimiento y detención de las siguientes personas](testing-following-and-stop-following-persons.md): describe los escenarios para probar la capacidad del proveedor de OSC para agregar a una persona como amigo o para quitar un amigo de la red social.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="1b4a4-113">[Probando amigos](testing-friends.md): describe las pruebas y los escenarios para comprobar que el proveedor de OSC devuelve correctamente datos de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="1b4a4-114">[Actividades de prueba](testing-activities.md): describe las pruebas y los escenarios para comprobar que el proveedor de OSC devuelve correctamente actividades de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b4a4-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="1b4a4-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="1b4a4-115">Reference</span></span>

- [<span data-ttu-id="1b4a4-116">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1b4a4-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="1b4a4-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="1b4a4-117">Related sections</span></span>

- [<span data-ttu-id="1b4a4-118">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="1b4a4-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="1b4a4-119">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="1b4a4-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="1b4a4-120">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="1b4a4-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="1b4a4-121">DePuración de un proveedor</span><span class="sxs-lookup"><span data-stu-id="1b4a4-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="1b4a4-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="1b4a4-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

