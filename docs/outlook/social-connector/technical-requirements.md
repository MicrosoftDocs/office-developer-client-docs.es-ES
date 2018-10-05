---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: En este tema se describe los lenguajes de programación compatibles, método y la visibilidad de COM devuelven requisitos de tipo y obtener información detallada de la extensibilidad de proveedor de Outlook Social Connector (OSC) DLL.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383117"
---
# <a name="technical-requirements"></a><span data-ttu-id="1457d-103">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="1457d-103">Technical requirements</span></span>

<span data-ttu-id="1457d-104">En este tema se describe los lenguajes de programación compatibles, método y la visibilidad de COM devuelven requisitos de tipo y obtener información detallada de la extensibilidad de proveedor de Outlook Social Connector (OSC) DLL.</span><span class="sxs-lookup"><span data-stu-id="1457d-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="1457d-105">Lenguaje de programación y los requisitos de COM</span><span class="sxs-lookup"><span data-stu-id="1457d-105">Programming language and COM requirements</span></span>

<span data-ttu-id="1457d-106">Puede crear un proveedor de OSC mediante lenguajes administrados como Visual C# o Visual Basic o lenguajes no administrados como Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1457d-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="1457d-107">Puede usar cualquier herramienta que puede crear un componente COM-visible DLL para desarrollar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1457d-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="1457d-108">La decisión de usar un lenguaje administrado o no administrado para desarrollar un proveedor debe tener en cuenta el tamaño de la descarga y las dependencias del paquete de instalación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1457d-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="1457d-109">Un proveedor de OSC debe ser visible a través de COM, tal como se define por lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1457d-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="1457d-110">Después de la instalación, se debe registrar un proveedor de OSC mediante el uso de registro de COM automático o regsvr32.</span><span class="sxs-lookup"><span data-stu-id="1457d-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="1457d-111">El registro de un proveedor de OSC DLL de COM registra el proveedor en HKCU o HKLM.</span><span class="sxs-lookup"><span data-stu-id="1457d-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="1457d-112">ProgID de un proveedor aparece registrado en `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="1457d-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="1457d-113">Un proveedor de OSC desarrollado en un lenguaje administrado es COM-visible.</span><span class="sxs-lookup"><span data-stu-id="1457d-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="1457d-114">Un proveedor de OSC debe agregar valores al registro de Windows que indican que el archivo DLL del proveedor admite apartamento de un único subproceso (STA) y apartamento multiproceso (MTA) modelos de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1457d-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="1457d-115">Para obtener más información acerca de los modelos de subprocesos de COM, vea [funcionamiento de OLE Threading modelos y descripciones](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="1457d-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="1457d-116">Métodos de extensibilidad de proveedores OSC deben devolver tipos primitivos como **cadena** o **bool**.</span><span class="sxs-lookup"><span data-stu-id="1457d-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="1457d-117">Determinadas **cadena** devolver valores deben cumplir con la definición del esquema para la extensibilidad de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="1457d-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="1457d-118">XML sólo se admite como un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1457d-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="1457d-119">Detalles de la extensibilidad del proveedor OSC DLL</span><span class="sxs-lookup"><span data-stu-id="1457d-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="1457d-120">El componente que admite la extensibilidad del proveedor OSC es la extensibilidad del proveedor OSC DLL.</span><span class="sxs-lookup"><span data-stu-id="1457d-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="1457d-121">Los programadores de terceros pueden generar archivos DLL de proveedor OSC mediante el uso de estas interfaces de extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="1457d-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="1457d-122">En la siguiente lista muestra los detalles de la extensibilidad del proveedor OSC DLL:</span><span class="sxs-lookup"><span data-stu-id="1457d-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="1457d-123">Nombre de archivo del archivo DLL de extensibilidad: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="1457d-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="1457d-124">Nombre descriptivo del archivo DLL de extensibilidad: extensibilidad de proveedor de Microsoft Outlook Social</span><span class="sxs-lookup"><span data-stu-id="1457d-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="1457d-125">Versión principal del archivo DLL de extensibilidad: 15.0</span><span class="sxs-lookup"><span data-stu-id="1457d-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="1457d-126">Versión de la biblioteca de tipos de archivo DLL de Extensibiilty: 1.1</span><span class="sxs-lookup"><span data-stu-id="1457d-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="1457d-127">Varias información técnica</span><span class="sxs-lookup"><span data-stu-id="1457d-127">Miscellaneous technical information</span></span>

<span data-ttu-id="1457d-128">No se admite JavaScript Object Notation (JSON) en el modelo de extensibilidad de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="1457d-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="1457d-129">No hay ninguna dependencia en un analizador de XML.</span><span class="sxs-lookup"><span data-stu-id="1457d-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="1457d-130">El proveedor de OSC puede usar un analizador de XML que se incluye con Office, como Microsoft XML Core Services (MSXML), use las funciones integradas en Microsoft .NET Framework de análisis de XML o usar un analizador XML de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="1457d-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1457d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1457d-131">See also</span></span>

- [<span data-ttu-id="1457d-132">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="1457d-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="1457d-133">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="1457d-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="1457d-134">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="1457d-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="1457d-135">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1457d-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

