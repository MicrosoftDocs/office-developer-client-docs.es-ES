---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: En este tema se describen los lenguajes de programación admitidos, los requisitos de visibilidad de COM y tipo de valor devuelto de los métodos y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329158"
---
# <a name="technical-requirements"></a><span data-ttu-id="b8ec1-103">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="b8ec1-103">Technical requirements</span></span>

<span data-ttu-id="b8ec1-104">En este tema se describen los lenguajes de programación admitidos, los requisitos de visibilidad de COM y tipo de valor devuelto de los métodos y los detalles de la DLL de extensibilidad del proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="b8ec1-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="b8ec1-105">Requisitos de COM y lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="b8ec1-105">Programming language and COM requirements</span></span>

<span data-ttu-id="b8ec1-106">Puede crear un proveedor OSC mediante lenguajes administrados como Visual C# o Visual Basic, o lenguajes no administrados como Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="b8ec1-107">Puede usar cualquier herramienta que pueda crear un componente DLL visible para COM para desarrollar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="b8ec1-108">La decisión de usar un lenguaje administrado o no administrado para desarrollar un proveedor debe tener en cuenta el tamaño de descarga y las dependencias del paquete de instalación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="b8ec1-109">Un proveedor OSC debe ser visible a través de COM, como se define en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8ec1-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="b8ec1-110">Después de la instalación, un proveedor OSC debe registrarse mediante el registro automático de COM o regsvr32.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="b8ec1-111">El registro COM de una DLL del proveedor de OSC registra el proveedor en HKCU o HKLM.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="b8ec1-112">El ProgID de un proveedor se registra `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`en.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="b8ec1-113">Un proveedor de OSC desarrollado en un lenguaje administrado es visible para COM.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="b8ec1-114">Un proveedor OSC debe agregar valores al registro de Windows que indiquen que el archivo DLL del proveedor admite modelos de subprocesos de apartamento de un solo subproceso (STA) y de Apartamento multiproceso (MTA).</span><span class="sxs-lookup"><span data-stu-id="b8ec1-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="b8ec1-115">Para obtener más información acerca de los modelos de subprocesos COM, vea deScripciones [and Works of OLE threadIng Models](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="b8ec1-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="b8ec1-116">Los métodos de la extensibilidad del proveedor OSC deben devolver tipos primitivos, como **String** o **bool**.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="b8ec1-117">Algunos valores devueltos por una **cadena** deben cumplir con la definición de esquema de la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="b8ec1-118">Solo se admite XML como un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="b8ec1-119">Detalles de la DLL de extensibilidad del proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="b8ec1-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="b8ec1-120">El componente que admite la extensibilidad del proveedor OSC es la DLL de extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="b8ec1-121">Los programadores de terceros pueden crear dll del proveedor OSC mediante el uso de estas interfaces de extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="b8ec1-122">En la siguiente lista se muestran los detalles de la DLL de extensibilidad del proveedor de OSC:</span><span class="sxs-lookup"><span data-stu-id="b8ec1-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="b8ec1-123">Nombre del archivo DLL de extensibilidad: socialprovider. dll</span><span class="sxs-lookup"><span data-stu-id="b8ec1-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="b8ec1-124">Nombre descriptivo de DLL de extensibilidad: extensibilidad del proveedor de Microsoft Outlook social</span><span class="sxs-lookup"><span data-stu-id="b8ec1-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="b8ec1-125">Versión principal del DLL de extensibilidad: 15,0</span><span class="sxs-lookup"><span data-stu-id="b8ec1-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="b8ec1-126">Versión de biblioteca de archivos DLL de Extensibiilty: 1,1</span><span class="sxs-lookup"><span data-stu-id="b8ec1-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="b8ec1-127">Información técnica diversa</span><span class="sxs-lookup"><span data-stu-id="b8ec1-127">Miscellaneous technical information</span></span>

<span data-ttu-id="b8ec1-128">La notación de objetos JavaScript (JSON) no se admite en el modelo de extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="b8ec1-129">No hay ninguna dependencia en un analizador XML.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="b8ec1-130">El proveedor OSC puede usar un analizador XML incluido en Office, como Microsoft XML Core Services (MSXML), usar las funciones de análisis XML integradas en Microsoft .NET Framework o usar un analizador XML de terceros.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8ec1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8ec1-131">See also</span></span>

- [<span data-ttu-id="b8ec1-132">Procedimientos recomendados para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="b8ec1-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="b8ec1-133">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="b8ec1-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="b8ec1-134">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b8ec1-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b8ec1-135">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b8ec1-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

