---
title: Integración de aplicaciones de mensajería instantánea con Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: En este artículo se describe cómo configurar una aplicación cliente de mensaje instantáneo (IM) para que se integra con las características sociales en Office 2013, incluyendo mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contacto.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821453"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="99048-103">Integración de aplicaciones de mensajería instantánea con Office</span><span class="sxs-lookup"><span data-stu-id="99048-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="99048-104">En este artículo se describe cómo configurar una aplicación cliente de mensaje instantáneo (IM) para que se integra con las características sociales en Office 2013, incluyendo mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="99048-105">Si tiene alguna pregunta o comentarios sobre este artículo técnico o los procesos que describe, puede ponerse en contacto con Microsoft directamente mediante el envío de un correo electrónico a [docthis@microsoft.com](mailto:docthis@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="99048-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="99048-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="99048-106">Introduction</span></span>
<span data-ttu-id="99048-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-107"></span></span>

<span data-ttu-id="99048-108">Office 2013 proporciona integración enriquecida con el cliente de mensajería instantánea a las aplicaciones, incluido Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="99048-108">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="99048-109">Esta integración proporciona a los usuarios con funciones de mensajería instantánea desde dentro de Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 y OneNote 2013, así como proporcionar integración de presencia en las páginas de SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="99048-109">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="99048-110">Los usuarios pueden ver la foto, el nombre, el estado de presencia y datos de contacto para las personas de su lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="99048-110">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="99048-111">Puede iniciar una sesión de mensajería instantánea, llamada de vídeo o llamada telefónica directamente desde la tarjeta de contacto (el elemento de la interfaz de usuario en Office 2013 que superficies, póngase en contacto con las opciones de información y comunicación).</span><span class="sxs-lookup"><span data-stu-id="99048-111">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="99048-112">Office 2013 facilita permanezcan conectados a sus contactos sin tener fuera de su correo electrónico o documentos.</span><span class="sxs-lookup"><span data-stu-id="99048-112">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="99048-113">En este artículo se utiliza el término aplicación de cliente de mensajería instantánea para hacer referencia específicamente a la aplicación instalada en el equipo del usuario que se comunica con el servicio de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-113">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="99048-114">Por ejemplo, Lync 2013 se considera una aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-114">For example, Lync 2013 is considered an IM client application.</span></span> <span data-ttu-id="99048-115">En este artículo no proporciona información detallada acerca de cómo se comunica la aplicación de cliente de mensajería instantánea para el servicio de mensajería instantánea o el propio servicio de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-115">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="99048-116">Puede personalizar una aplicación de cliente de mensajería instantánea, por lo que se comunica con Office.</span><span class="sxs-lookup"><span data-stu-id="99048-116">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="99048-117">En concreto, puede modificar la aplicación de mensajería instantánea para que muestre la información siguiente dentro de la interfaz de usuario de Office:</span><span class="sxs-lookup"><span data-stu-id="99048-117">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="99048-118">Foto del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-118">Contact photo.</span></span>
    
- <span data-ttu-id="99048-119">Nombre del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-119">Contact name.</span></span>
    
- <span data-ttu-id="99048-120">Póngase en contacto con nota de estado personal.</span><span class="sxs-lookup"><span data-stu-id="99048-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="99048-121">Póngase en contacto con el estado de presencia.</span><span class="sxs-lookup"><span data-stu-id="99048-121">Contact presence status.</span></span>
    
- <span data-ttu-id="99048-122">Póngase en contacto con la cadena de disponibilidad (por ejemplo, "Disponible" o "fuera de la oficina").</span><span class="sxs-lookup"><span data-stu-id="99048-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="99048-123">Póngase en contacto con la cadena de capacidad (por ejemplo, "vídeo listo").</span><span class="sxs-lookup"><span data-stu-id="99048-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="99048-124">Inicio de mensajería instantánea de un solo clic.</span><span class="sxs-lookup"><span data-stu-id="99048-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="99048-125">Inicio de la llamada de vídeo de un solo clic.</span><span class="sxs-lookup"><span data-stu-id="99048-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="99048-126">Inicio de llamadas de teléfono de un solo clic (incluidos SIP, número de teléfono, correo de voz y nuevo número de llamada).</span><span class="sxs-lookup"><span data-stu-id="99048-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="99048-127">Administración de contactos (agregar al grupo de mensajería instantánea).</span><span class="sxs-lookup"><span data-stu-id="99048-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="99048-128">Póngase en contacto con ubicación y zona horaria.</span><span class="sxs-lookup"><span data-stu-id="99048-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="99048-129">Datos de contacto, número de teléfono, dirección de correo electrónico, título y nombre de la compañía.</span><span class="sxs-lookup"><span data-stu-id="99048-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="99048-130">**En la figura 1. Tarjeta de contacto de Office 2013**</span><span class="sxs-lookup"><span data-stu-id="99048-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="99048-131">![La tarjeta de personas en Office 2013] (media/ocom15_peoplecard.png "La tarjeta de personas en Office 2013")</span><span class="sxs-lookup"><span data-stu-id="99048-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="99048-132">Para habilitar esta integración con Office, una aplicación de cliente de mensajería instantánea debe implementar un conjunto de interfaces que proporciona Office para conectarse a ella.</span><span class="sxs-lookup"><span data-stu-id="99048-132">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="99048-133">Las API para esta integración se incluyen en el espacio de nombres [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que se encuentra en el archivo Microsoft.Office.UC.dll, que se instala con las versiones de Office 2013 que incluyen Lync / Skype para la empresa.</span><span class="sxs-lookup"><span data-stu-id="99048-133">The APIs for this integration are included in the [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="99048-134">El espacio de nombres **UCCollaborationLib** incluye las interfaces que debe implementar para integrar con Office.</span><span class="sxs-lookup"><span data-stu-id="99048-134">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="99048-135">La biblioteca de tipos para las interfaces necesarias está incrustada en Lync 2013/Skype para la empresa.</span><span class="sxs-lookup"><span data-stu-id="99048-135">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="99048-136">Para integradores de sistemas de terceros, esto funciona sólo cuando Lync 2013 y Skype para la empresa están instalados en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="99048-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="99048-137">Si va a integrar con Office Standard, debe extraer la biblioteca de tipos e instalarlo en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="99048-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="99048-138">El [SDK de Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) incluye el archivo Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="99048-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="99048-139">Un conjunto de aplicaciones de Office 2010 puede integrar de forma similar con una aplicación de proveedor de mensajería instantánea de terceros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 y SharePoint Server 2010 (mediante un control ActiveX).</span><span class="sxs-lookup"><span data-stu-id="99048-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="99048-140">Muchos de los pasos necesarios para la integración con Office 2013 aplican también a Office 2010.</span><span class="sxs-lookup"><span data-stu-id="99048-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="99048-141">Hay varias diferencias claves en cómo se integra Office 2010 con una aplicación de proveedor de mensajería instantánea:</span><span class="sxs-lookup"><span data-stu-id="99048-141">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="99048-142">Office 2010 no mostrar fotografía del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-142">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="99048-143">Debe descargar el archivo Microsoft.Office.Uc.dll por separado desde Office 2010.</span><span class="sxs-lookup"><span data-stu-id="99048-143">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="99048-144">El [SDK de Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) incluye el archivo Microsoft.Office.UC.dll para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="99048-144">The [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="99048-145">Cuando la aplicación de Office, llama al método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) en la aplicación de cliente de mensajería instantánea, se pasa en la cadena "14.0.0.0".</span><span class="sxs-lookup"><span data-stu-id="99048-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="99048-146">Office 2010 enumera todos los grupos y contactos tan pronto como se conecta a una aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-146">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="99048-147">¿Cómo se integra Office con una aplicación de cliente de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="99048-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="99048-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-148"></span></span>

<span data-ttu-id="99048-149">Cuando se inicia una aplicación de Office 2013, pasa por el siguiente proceso para integrarse con la aplicación de cliente de mensajería instantánea predeterminada:</span><span class="sxs-lookup"><span data-stu-id="99048-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="99048-150">Comprueba el registro para descubrir la aplicación de cliente de mensajería instantánea de forma predeterminada y, a continuación, se conecta a él.</span><span class="sxs-lookup"><span data-stu-id="99048-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="99048-151">Se autentica con la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="99048-152">Se conecta a interfaces específicas que se exponen con la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="99048-153">Determina las capacidades del usuario ha iniciado sesión actualmente (usuario local), incluida la introducción de los contactos del usuario, determinar la presencia del usuario y determinar las capacidades de mensajería instantánea del usuario (mensajería instantánea, chat de vídeo, VOIP y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="99048-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="99048-154">Obtiene información de presencia de los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="99048-155">Cuando se cierra la aplicación de cliente de mensajería instantánea, la aplicación de Office 2013 se desconecta en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="99048-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="99048-156">Detección de la aplicación de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="99048-156">Discovering the IM application</span></span>

<span data-ttu-id="99048-157">La aplicación de Office busca varias teclas específicas y las entradas del registro para detectar la aplicación de cliente de mensajería instantánea de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="99048-157">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="99048-158">Si detecta una aplicación de cliente de mensajería instantánea de forma predeterminada, a continuación, intenta conectarse a ella.</span><span class="sxs-lookup"><span data-stu-id="99048-158">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="99048-159">El proceso que realiza la aplicación de Office para detectar la aplicación de cliente de mensajería instantánea predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="99048-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="99048-160">La aplicación de Office comprueba si se establece la subclave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp en el registro y lee el nombre de la aplicación enumerados ahí.</span><span class="sxs-lookup"><span data-stu-id="99048-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="99048-161">A continuación, la aplicación de Office lee la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning y supervisa el valor para que los cambios.</span><span class="sxs-lookup"><span data-stu-id="99048-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="99048-162">A continuación, la aplicación de Office lee la clave del registro de proveedores de contenido\ HKEY_LOCAL_MACHINE\Software\IM _nombre de la aplicación_ y obtiene los valores de identificador (CLSID) de nombre de proceso y la clase almacenados en ella.</span><span class="sxs-lookup"><span data-stu-id="99048-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="99048-163">Una vez que la aplicación de cliente de mensajería instantánea ha completado correctamente la secuencia de inicio y registrado todas las clases correctamente para la integración de presencia, se establece la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning a "2", que indica que se está ejecutando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="99048-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="99048-164">Cuando la aplicación de Office detecta que se ha establecido la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning a "2", se revisa la lista de procesos en ejecución en el equipo para el nombre del proceso de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="99048-165">Una vez que la aplicación de Office encuentra el proceso que utiliza la aplicación de cliente de mensajería instantánea, la aplicación de Office llama a **CoCreateInstance** utilizando el CLSID para establecer una conexión a la aplicación de cliente de mensajería instantánea como un servidor COM fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="99048-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="99048-166">Autenticar la conexión a la aplicación de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="99048-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="99048-167">Después de la aplicación de Office establece una conexión a la aplicación de cliente de mensajería instantánea, a continuación, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99048-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="99048-168">La aplicación de Office llama a método [IUnknown:: QueryInterface](http://msdn.microsoft.com/es-es/library/ms682521%28v=VS.85%29.aspx) para comprobar si la interfaz [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) .</span><span class="sxs-lookup"><span data-stu-id="99048-168">The Office application calls [IUnknown::QueryInterface](http://msdn.microsoft.com/es-es/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="99048-169">La aplicación de Office, a continuación, llama al método **IUCOfficeIntegration.GetAuthenticationInfo** , pasando la versión más alta de integración compatibles (por ejemplo, "15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="99048-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="99048-170">Si la aplicación de cliente de mensajería instantánea es compatible con la versión de Office que se pasó como un parámetro, la aplicación devuelve la siguiente cadena XML codificado de forma rígida al código de llamada:</span><span class="sxs-lookup"><span data-stu-id="99048-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="99048-171">Por razones de herencia, la aplicación de cliente de mensajería instantánea debe devolver el valor exacto `<authenticationinfo>` a la llamada a **GetAuthenticationInfo** si es compatible con la versión de Office que se pasó como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="99048-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="99048-172">Si se produce un error en la aplicación de cliente de mensajería instantánea devolver un valor, la aplicación de Office llama al método **GetAuthenticationInfo** con la última versión compatible de Office (por ejemplo, "14.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="99048-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="99048-173">Una vez que Office determina que la aplicación de cliente de mensajería instantánea admite la integración de mensajería instantánea y presencia, se conecta a un conjunto de interfaces para finalizar la inicialización requerido.</span><span class="sxs-lookup"><span data-stu-id="99048-173">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="99048-174">(Para obtener más información, consulte [Connecting to interfaces necesarias](#off15_IMIntegration_HowConnect)).</span><span class="sxs-lookup"><span data-stu-id="99048-174">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="99048-175">Si la aplicación de Office detecta un error en cualquiera de los pasos anteriores, deshace los y no se ha establecido la integración de presencia de nuevo durante la sesión de la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="99048-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="99048-176">Que se conectan a interfaces necesarias</span><span class="sxs-lookup"><span data-stu-id="99048-176">Connecting to required interfaces</span></span>
<span data-ttu-id="99048-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-177"></span></span>

<span data-ttu-id="99048-178">Después de la autenticación de la conexión a la aplicación de cliente de mensajería instantánea, la aplicación de Office intenta conectarse a un conjunto de interfaces necesarias que debe exponer la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-178">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="99048-179">La aplicación de Office se lleva a cabo mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="99048-179">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="99048-180">La aplicación de Office obtiene que un objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) llamando al método **IUCOfficeIntegration.GetInterface** , pasando el **oiInterfaceLyncClient** constante de la enumeración [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) .</span><span class="sxs-lookup"><span data-stu-id="99048-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="99048-181">La aplicación de Office obtiene que un objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) llamando al método **IUCOfficeIntegration.GetInterface** , pasando el **oiInterfaceAutomation** constante de la enumeración **OIInterface** .</span><span class="sxs-lookup"><span data-stu-id="99048-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="99048-182">La aplicación de Office se configura el agente de escucha de eventos de [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) .</span><span class="sxs-lookup"><span data-stu-id="99048-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="99048-183">La aplicación de Office se configura el agente de escucha de eventos de [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) .</span><span class="sxs-lookup"><span data-stu-id="99048-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="99048-184">La aplicación de Office, obtiene el estado de inicio de sesión de la aplicación de cliente de mensajería instantánea mediante el acceso a la propiedad **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="99048-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="99048-185">La aplicación de Office obtiene las capacidades de la aplicación de cliente de mensajería instantánea llamando al método **IUCOfficeIntegration.GetSupportedFeatures** , que devuelve un indicador de la enumeración [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="99048-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="99048-186">La aplicación de Office tiene acceso a la propiedad **ILyncClient.Self** para obtener una referencia a un objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="99048-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="99048-187">Recuperación de las capacidades del usuario local</span><span class="sxs-lookup"><span data-stu-id="99048-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="99048-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-188"></span></span>

<span data-ttu-id="99048-189">La aplicación de Office obtiene las capacidades del usuario local haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99048-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="99048-190">Si la aplicación de cliente de mensajería instantánea es compatible con la interfaz **IClient2** , Office intenta obtener un objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) mediante el acceso a la propiedad **IClient2.PrivateContactManager** .</span><span class="sxs-lookup"><span data-stu-id="99048-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="99048-191">Si la aplicación de mensajería instantánea no es compatible con la interfaz **IClient2** , aplicación de Office obtiene un objeto **IContactManager** mediante el acceso a la propiedad **ILyncClient.ContactManager** .</span><span class="sxs-lookup"><span data-stu-id="99048-191">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="99048-192">La aplicación de cliente de mensajería instantánea correctamente debe devolver un objeto **IContactManager** antes de pueden establecer cualquier otras funciones de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-192">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="99048-193">La aplicación de Office se tiene acceso a la propiedad **ILyncClient.Uri** y, a continuación, llama a **IContactManager.GetContactByUri** para obtener el objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="99048-194">A continuación, la aplicación de Office realiza varias llamadas a **IContact.CanStart** para establecer las capacidades del usuario local, pasando los valores para **ModalityTypes.ucModalityInstantMessage** y **ModalityTypes.ucModalityAudioVideo** sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="99048-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="99048-195">Recuperación de presencia de los contactos</span><span class="sxs-lookup"><span data-stu-id="99048-195">Retrieving contact presence</span></span>
<span data-ttu-id="99048-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-196"></span></span>

<span data-ttu-id="99048-197">La aplicación de Office obtiene la presencia de los contactos, incluido el usuario local, haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99048-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="99048-198">La aplicación de Office llama a **IContact.GetContactInformation** para obtener un elemento de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="99048-199">A continuación, la aplicación de Office se suscribe a los cambios de estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-199">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="99048-200">Se llama **IContactManager.CreateSubscription** para obtener un objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="99048-200">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="99048-201">A continuación, llama a **IContactSubscription.AddContact** para agregar el contacto a la suscripción y, a continuación, llama a **IContactSubscription.Subscribe** para obtener los cambios en el estado del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-201">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="99048-202">Si la aplicación de mensajería instantánea admite **IContact2**, Office intenta obtener información de presencia mediante una llamada a **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="99048-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="99048-203">A continuación, la aplicación de Office recupera las propiedades de presencia del contacto mediante una llamada a **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="99048-203">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="99048-204">La aplicación de Office puede obtener un segundo conjunto de propiedades de presencia mediante el acceso a la propiedad **IContact.Settings** .</span><span class="sxs-lookup"><span data-stu-id="99048-204">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="99048-205">Por último, la aplicación de Office obtiene la pertenencia a un grupo del contacto mediante el acceso a la propiedad **IContact.CustomGroups** .</span><span class="sxs-lookup"><span data-stu-id="99048-205">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="99048-206">Esto devuelve una colección de [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que todos los objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que pertenece el contacto incluye.</span><span class="sxs-lookup"><span data-stu-id="99048-206">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="99048-207">Desconectar de la aplicación de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="99048-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="99048-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-208"></span></span>

<span data-ttu-id="99048-209">Cuando la aplicación de Office 2013 detecta el evento **OnShuttingDown** desde la aplicación de mensajería instantánea, desconecta en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="99048-209">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="99048-210">Sin embargo, si la aplicación de Office se cierra antes de la aplicación de mensajería instantánea, la aplicación de Office no garantiza que la conexión se limpien.</span><span class="sxs-lookup"><span data-stu-id="99048-210">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="99048-211">La aplicación de mensajería instantánea debe controlar pérdidas de conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="99048-211">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="99048-212">Las entradas y las claves del registro de configuración</span><span class="sxs-lookup"><span data-stu-id="99048-212">Setting registry keys and entries</span></span>
<span data-ttu-id="99048-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-213"></span></span>

<span data-ttu-id="99048-214">Como se mencionó anteriormente, las aplicaciones de mensajería instantánea capaz de Office 2013 buscan teclas específicas, entradas y valores del registro para detectar la aplicación de cliente de mensajería instantánea para conectarse a.</span><span class="sxs-lookup"><span data-stu-id="99048-214">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="99048-215">Estos valores del registro proporcionan la aplicación de Office con el nombre del proceso y el CLSID de la clase que actúa como el punto de entrada al modelo de objetos de la aplicación de cliente de mensajería instantánea (es decir, la clase que implementa la interfaz **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="99048-215">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="99048-216">La aplicación de Office crea co-autoría dicha clase y se conecta como un cliente para el servidor COM fuera de proceso en la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-216">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="99048-217">Use la tabla 1 para identificar las claves, las entradas y los valores que deben escribirse en el registro para integrar una aplicación de cliente de mensajería instantánea con Office.</span><span class="sxs-lookup"><span data-stu-id="99048-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="99048-218">**La tabla 1. Claves de registro para la configuración de la aplicación de cliente de mensajería instantánea predeterminada**</span><span class="sxs-lookup"><span data-stu-id="99048-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="99048-219">**Clave**</span><span class="sxs-lookup"><span data-stu-id="99048-219">**Key**</span></span>|<span data-ttu-id="99048-220">**Entry**</span><span class="sxs-lookup"><span data-stu-id="99048-220">**Entry**</span></span>|<span data-ttu-id="99048-221">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99048-221">**Type**</span></span>|<span data-ttu-id="99048-222">**Valor**</span><span class="sxs-lookup"><span data-stu-id="99048-222">**Value**</span></span>|<span data-ttu-id="99048-223">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="99048-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="99048-224">Proveedores de HKEY_LOCAL_MACHINE\Software\IM\\< nombre de la aplicación\></span><span class="sxs-lookup"><span data-stu-id="99048-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="99048-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="99048-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="99048-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99048-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="99048-227">El nombre de la aplicación de cliente de mensajería instantánea de otro fabricante.</span><span class="sxs-lookup"><span data-stu-id="99048-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="99048-228">Mensajería instantánea de Litware 2012</span><span class="sxs-lookup"><span data-stu-id="99048-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="99048-229">Nombre de proceso</span><span class="sxs-lookup"><span data-stu-id="99048-229">ProcessName</span></span>  <br/> |<span data-ttu-id="99048-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99048-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="99048-231">El nombre del proceso de la aplicación de cliente de mensajería instantánea de otro fabricante.</span><span class="sxs-lookup"><span data-stu-id="99048-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="99048-232">Litware.exe</span><span class="sxs-lookup"><span data-stu-id="99048-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="99048-233">GUID</span><span class="sxs-lookup"><span data-stu-id="99048-233">GUID</span></span>  <br/> |<span data-ttu-id="99048-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99048-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="99048-235">Un identificador de clase (CLSID) para la raíz, clase cocreatable en la aplicación de mensajería instantánea (es decir, la clase que implementa la interfaz **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="99048-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="99048-236">(GUID)</span><span class="sxs-lookup"><span data-stu-id="99048-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="99048-237">Proveedores de HKEY_CURRENT_USER\Software\IM</span><span class="sxs-lookup"><span data-stu-id="99048-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="99048-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="99048-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="99048-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99048-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="99048-240">El nombre de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-240">The name of the IM client application.</span></span> <span data-ttu-id="99048-241">Esto debe ser el mismo que el nombre en la clave de registro de nivel superior (subárbol) en HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="99048-241">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="99048-242">Litware</span><span class="sxs-lookup"><span data-stu-id="99048-242">Litware</span></span>  <br/> |
|<span data-ttu-id="99048-243">Proveedores de HKEY_CURRENT_USER\Software\IM\\< nombre de la aplicación\></span><span class="sxs-lookup"><span data-stu-id="99048-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="99048-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="99048-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="99048-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="99048-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="99048-246">Un valor entero entre 0 y 2:</span><span class="sxs-lookup"><span data-stu-id="99048-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="99048-247">0: no está ejecutando</span><span class="sxs-lookup"><span data-stu-id="99048-247">0—Not running</span></span>  <br/>  <span data-ttu-id="99048-248">1: inicio</span><span class="sxs-lookup"><span data-stu-id="99048-248">1—Starting</span></span>  <br/>  <span data-ttu-id="99048-249">2: ejecuta</span><span class="sxs-lookup"><span data-stu-id="99048-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="99048-250">**Nota**: la clave del registro de nombre de aplicación debe ser el mismo que el valor de la entrada DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="99048-250">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="99048-251">Implementar las interfaces necesarias para la integración con Office</span><span class="sxs-lookup"><span data-stu-id="99048-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="99048-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-252"></span></span>

<span data-ttu-id="99048-253">Existen tres interfaces desde el espacio de nombres **UCCollaborationLib** que debe implementar el archivo ejecutable (o servidor COM) de una aplicación de cliente de mensajería instantánea para que puede integrar con Office.</span><span class="sxs-lookup"><span data-stu-id="99048-253">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="99048-254">Si no se implementan estas interfaces, deshace la aplicación de Office durante el proceso de inicialización y no se establece la conexión con la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-254">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="99048-255">Las interfaces necesarias son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="99048-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="99048-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration), aunque no es necesario, la interfaz de **_IUCOfficeIntegrationEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="99048-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="99048-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient), aunque no es necesario, la interfaz de **_ILyncClientEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="99048-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="99048-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="99048-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="99048-259">Interfaz IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="99048-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="99048-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-260"></span></span>

<span data-ttu-id="99048-261">La interfaz de **IUCOfficeIntegration** proporciona el punto de entrada para una aplicación de Office para conectarse a la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-261">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="99048-262">La interfaz define tres métodos que llama una aplicación de Office como parte del proceso de inicio de una conexión con la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-262">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="99048-263">La clase que implementa la interfaz **IUCOfficeIntegration** debe ser co-autoría creable para que Office co-autoría puede crear una instancia de él.</span><span class="sxs-lookup"><span data-stu-id="99048-263">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="99048-264">Además, debe exponer el CLSID que se escribe como el valor de la entrada de GUID en la clave del registro de proveedores de contenido\ HKEY_LOCAL_MACHINE\Software\IM _nombre de la aplicación_ .</span><span class="sxs-lookup"><span data-stu-id="99048-264">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="99048-265">La clase que hereda de **IUCOfficeIntegration** también debe implementar la interfaz **_IUCOfficeIntegrationEvents** .</span><span class="sxs-lookup"><span data-stu-id="99048-265">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="99048-266">La interfaz **_IUCOfficeIntegrationEvents** contiene a los miembros que exponen los controladores de eventos de la interfaz **IUCOfficeIntegration** .</span><span class="sxs-lookup"><span data-stu-id="99048-266">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="99048-267">La tabla 2 muestra a los miembros que deben implementarse en la clase que hereda de **IUCOfficeIntegration** y **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="99048-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-268">Para obtener más información acerca de la **IUCOfficeIntegration** y **_IUCOfficeIntegrationEvents** interfaces y sus miembros, vea [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) y [UCCollaborationLib._IUCOfficeIntegrationEvents ](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="99048-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="99048-269">**Tabla 2. Implementación de las interfaces IUCOfficeIntegration y _IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="99048-270">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="99048-270">**Interface**</span></span>|<span data-ttu-id="99048-271">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-271">**Member**</span></span>|<span data-ttu-id="99048-272">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99048-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="99048-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="99048-274">**GetAuthenticationInfo** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="99048-275">Obtiene la cadena de información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="99048-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="99048-276">**GetInterface** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="99048-277">Obtiene la interfaz de una versión concreta.</span><span class="sxs-lookup"><span data-stu-id="99048-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="99048-278">**GetSupportedFeatures** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="99048-279">Obtiene las características de integración de Office admitidas.</span><span class="sxs-lookup"><span data-stu-id="99048-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="99048-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="99048-281">**OnShuttingDown** (evento)</span><span class="sxs-lookup"><span data-stu-id="99048-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="99048-282">El evento que se produce cuando la aplicación de cliente de mensajería instantánea está intentando apagar.</span><span class="sxs-lookup"><span data-stu-id="99048-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="99048-283">Use el siguiente código para definir una clase que hereda de las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegration** dentro de una aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="99048-284">El método **GetAuthenticationInfo** toma una cadena como un argumento para el parámetro de _versión_ .</span><span class="sxs-lookup"><span data-stu-id="99048-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="99048-285">Cuando la aplicación de Office llama a este método, se pasa en uno de dos cadenas para el argumento, según la versión de Office.</span><span class="sxs-lookup"><span data-stu-id="99048-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="99048-286">Cuando la aplicación de Office proporciona el método con la versión de Office que admite la aplicación de cliente de mensajería instantánea (es decir, admite la funcionalidad), el método **GetAuthenticationInfo** devuelve una cadena XML codificado de forma rígida `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="99048-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="99048-287">Use el siguiente código para implementar el método **GetAuthentication** dentro del código de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="99048-288">El método **GetInterface** referencias a las clases desplazará al código de llamada, dependiendo de lo que se pasa como un argumento para el parámetro de _interfaz_ .</span><span class="sxs-lookup"><span data-stu-id="99048-288">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="99048-289">Cuando una aplicación de Office llama el método **GetInterface** , se pasa en uno de dos valores para el parámetro de interfaz: la constante **oiInterfaceILyncClient** (1) o bien la constante **oiInterfaceIAutomation** (2) de la [ UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) (enumeración).</span><span class="sxs-lookup"><span data-stu-id="99048-289">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="99048-290">Si la aplicación de Office pasa la constante **oiInterfaceILyncClient** , el método **GetInterface** devuelve una referencia a una clase que implementa la interfaz **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="99048-290">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="99048-291">Si la aplicación de Office pasa la constante **oiInterfaceIAutomation** , el método **GetInterface** devuelve una clase que implementa la interfaz **IAutomation** .</span><span class="sxs-lookup"><span data-stu-id="99048-291">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="99048-292">Use el siguiente ejemplo de código para implementar el método **GetInterface** dentro del código de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="99048-293">El método **GetSupportedFeatures** devuelve información acerca de las características de mensajería instantánea que admite la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-293">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="99048-294">Toma una cadena para su único parámetro, _versión_.</span><span class="sxs-lookup"><span data-stu-id="99048-294">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="99048-295">Cuando la aplicación de Office llama al método de **GetSupportFeatures** , el método devuelve un valor de la enumeración [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="99048-295">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="99048-296">El valor devuelto especifica las funciones del cliente de mensajería instantánea, donde cada función de la aplicación de cliente de mensajería instantánea se indica a la aplicación de Office mediante la adición de un marcador para el valor.</span><span class="sxs-lookup"><span data-stu-id="99048-296">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="99048-297">Aplicaciones de Office 2013 omitir las siguientes constantes en la enumeración **OIFeature** :</span><span class="sxs-lookup"><span data-stu-id="99048-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="99048-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="99048-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="99048-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="99048-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="99048-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="99048-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="99048-301">Use el siguiente ejemplo de código para implementar el método **GetSupportFeatures** dentro del código de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="99048-302">Interfaz ILyncClient</span><span class="sxs-lookup"><span data-stu-id="99048-302">ILyncClient interface</span></span>
<span data-ttu-id="99048-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-303"></span></span>

<span data-ttu-id="99048-304">La interfaz de **ILyncClient** se asigna a las capacidades de la propia aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-304">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="99048-305">Expone propiedades que hacen referencia a la persona que ha iniciado sesión en la aplicación (el usuario local, representado por la interfaz de [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), el estado de la aplicación, la lista de contactos para el usuario local y varias opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="99048-305">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="99048-306">Cuando intenta conectarse a la aplicación de cliente de mensajería instantánea, la aplicación de Office obtiene una referencia a un objeto que implementa la interfaz **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="99048-306">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="99048-307">Desde esa referencia, Office puede tener acceso a gran parte de la funcionalidad de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-307">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="99048-308">Además, la clase que implementa la interfaz **ILyncClient** también debe implementar la interfaz **_ILyncClientEvents** .</span><span class="sxs-lookup"><span data-stu-id="99048-308">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="99048-309">La interfaz **_ILyncClientEvents** expone algunos de los eventos que son necesarios para supervisar el estado de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-309">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="99048-310">Tabla 3 se muestran a los miembros que deben implementarse en la clase que hereda de **ILyncClient** y **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="99048-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-311">Cualquier miembro de la **ILyncClient** o ** \_ILyncClientEvents** interfaz no aparece en la tabla debe estar presente pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-311">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-312">Los miembros que están presentes, pero no implementado pueden producir una **NotImplementedException** o **E\_NOTIMPL** error.</span><span class="sxs-lookup"><span data-stu-id="99048-312">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="99048-313">Para obtener más información acerca de la **ILyncClient** y **_ILyncClientEvents** interfaces y sus miembros, vea [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) y [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="99048-313">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="99048-314">**Tabla 3. Implementación de interfaces ILyncClient y ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="99048-315">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="99048-315">**Interface**</span></span>|<span data-ttu-id="99048-316">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-316">**Member**</span></span>|<span data-ttu-id="99048-317">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99048-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="99048-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="99048-319">**ContactManager** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="99048-320">Obtiene el Administrador de grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="99048-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="99048-321">**ConversationManager** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="99048-322">Obtiene el Administrador de conversaciones.</span><span class="sxs-lookup"><span data-stu-id="99048-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="99048-323">**Self** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-323">**Self** property</span></span>  <br/> |<span data-ttu-id="99048-324">Obtiene el objeto **Self** .</span><span class="sxs-lookup"><span data-stu-id="99048-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="99048-325">**Inicio de sesión** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="99048-326">Inicia el aplicación de cliente de mensajería instantánea inicio de sesión de proceso con una disponibilidad específica.</span><span class="sxs-lookup"><span data-stu-id="99048-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="99048-327">**Estado** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-327">**State** property</span></span>  <br/> |<span data-ttu-id="99048-328">Obtiene el estado actual de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="99048-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="99048-329">**URI** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="99048-330">Obtiene el identificador URI de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="99048-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="99048-332">**OnStateChanged** (evento)</span><span class="sxs-lookup"><span data-stu-id="99048-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="99048-333">Se produce cuando cambia el estado de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-333">Raised when the IM client application state changes.</span></span> <span data-ttu-id="99048-334">Debe controlar este evento y obtenga la propiedad **eventData.NewState** .</span><span class="sxs-lookup"><span data-stu-id="99048-334">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="99048-335">El evento se desencadena para todos los procesos vinculados a una instancia de una aplicación de cliente de mensajería instantánea cuando cualquier subsistema en la aplicación hace que el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="99048-335">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="99048-336">Durante el proceso de inicialización, Office obtiene acceso a la propiedad **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="99048-336">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="99048-337">Esta propiedad debe devolver un valor de la enumeración [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) .</span><span class="sxs-lookup"><span data-stu-id="99048-337">This property needs to return a value from the [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="99048-338">La propiedad **State** almacena el estado actual de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-338">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="99048-339">Debe establecer y actualizan a lo largo de la sesión de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-339">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="99048-340">Cuando el mensaje instantáneo aplicación cliente inicia sesión, cierra la sesión, o se apaga, debe establecer la propiedad **State** .</span><span class="sxs-lookup"><span data-stu-id="99048-340">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="99048-341">Es mejor establecer esta propiedad dentro de los métodos **ILyncClient.SignIn** y **ILyncClient.SignOut** , tal y como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="99048-341">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="99048-342">En el ejemplo de código siguiente se muestra cómo configurar el agente de escucha de eventos mediante el _ **ILyncClientEvents** y _ **IUCOfficeIntegrationEvents** interfaces.</span><span class="sxs-lookup"><span data-stu-id="99048-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="99048-343">Interfaz IAutomation</span><span class="sxs-lookup"><span data-stu-id="99048-343">IAutomation interface</span></span>
<span data-ttu-id="99048-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-344"></span></span>

<span data-ttu-id="99048-345">La interfaz de **IAutomation** automatiza las características de la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-345">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="99048-346">Se puede usar para iniciar conversaciones, participar en conferencias y proporcionar contexto de ventana de extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="99048-346">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="99048-347">La tabla 4 muestra a los miembros que deben implementarse en la clase que hereda de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="99048-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-348">Cualquier miembro de la interfaz de **IAutomation** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-349">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="99048-350">Para obtener más información acerca de la interfaz de **IAutomation** y sus miembros, vea [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="99048-350">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="99048-351">**Tabla 4. Implementación de interfaz IAutomation**</span><span class="sxs-lookup"><span data-stu-id="99048-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="99048-352">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-352">**Member**</span></span>|<span data-ttu-id="99048-353">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-354">**StartConversation** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="99048-355">Inicia una conversación mediante la modalidad de conversación especificado.</span><span class="sxs-lookup"><span data-stu-id="99048-355">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="99048-356">Se devuelve una instancia de **IConversationWindow** .</span><span class="sxs-lookup"><span data-stu-id="99048-356">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="99048-357">Implementación de la integración de presencia de los contactos</span><span class="sxs-lookup"><span data-stu-id="99048-357">Implementing contact presence integration</span></span>
<span data-ttu-id="99048-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-358"></span></span>

<span data-ttu-id="99048-359">Además de las tres interfaces necesarias que se ha mencionado anteriormente, hay varias otras interfaces que son importantes para habilitar la funcionalidad de presencia de los contactos en Office.</span><span class="sxs-lookup"><span data-stu-id="99048-359">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="99048-360">Estos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="99048-360">These include the following:</span></span>
  
- <span data-ttu-id="99048-361">La interfaz [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) o **IContact2** .</span><span class="sxs-lookup"><span data-stu-id="99048-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="99048-362">La interfaz [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="99048-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="99048-363">Las interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) y [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) .</span><span class="sxs-lookup"><span data-stu-id="99048-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="99048-364">Las interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) y [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) .</span><span class="sxs-lookup"><span data-stu-id="99048-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="99048-365">La interfaz [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="99048-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="99048-366">La interfaz [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) .</span><span class="sxs-lookup"><span data-stu-id="99048-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="99048-367">La interfaz de [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="99048-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="99048-368">Interfaz IContact</span><span class="sxs-lookup"><span data-stu-id="99048-368">IContact interface</span></span>
<span data-ttu-id="99048-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-369"></span></span>

<span data-ttu-id="99048-370">La interfaz **IContact** representa un usuario de aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-370">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="99048-371">La interfaz expone la presencia, modalidades disponibles, pertenencia a grupos y las propiedades de tipo de contacto de un usuario.</span><span class="sxs-lookup"><span data-stu-id="99048-371">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="99048-372">Para iniciar una conversación con otro usuario, debe proporcionar esa instancia de usuario de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="99048-372">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="99048-373">Tabla 5 se muestran a los miembros que deben implementarse en la clase que hereda de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="99048-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-374">Cualquier miembro de la interfaz de **IContact** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-375">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="99048-376">Para obtener más información acerca de la interfaz de **IContact** y sus miembros, vea [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="99048-376">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="99048-377">**Tabla 5. Implementación de la interfaz de IContact**</span><span class="sxs-lookup"><span data-stu-id="99048-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="99048-378">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-378">**Member**</span></span>|<span data-ttu-id="99048-379">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-380">**CanStart** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="99048-381">Devuelve **true** si se puede iniciar un tipo determinado de modalidad en el contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="99048-382">**GetContactInformation** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="99048-383">Obtiene un elemento de la presencia de un contacto de la publicación.</span><span class="sxs-lookup"><span data-stu-id="99048-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="99048-384">**BatchGetContactInformation** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="99048-385">Obtiene varios elementos de la presencia de un contacto de la publicación.</span><span class="sxs-lookup"><span data-stu-id="99048-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="99048-386">**Settings** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="99048-387">Obtiene una colección de propiedades de contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="99048-388">**CustomGroups** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="99048-389">Obtiene una colección de grupos que el contacto es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="99048-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="99048-390">Durante el proceso de inicialización, la aplicación de Office llama al método de **IContact.CanStart** para determinar las capacidades de mensajería instantánea para el usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-390">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="99048-391">El método **CanStart** utiliza un indicador de la enumeración [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como un argumento para el parámetro de_modalityTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="99048-391">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter.</span></span> <span data-ttu-id="99048-392">Si el usuario actual puede integrarse en la modalidad solicitada (es decir, el usuario es capaz de mensajería instantánea, audio y vídeo de mensajería o uso compartido de aplicaciones), el método **CanStart** devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="99048-392">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="99048-393">El método **GetContactInformation** recupera información sobre el contacto desde el objeto **IContact** .</span><span class="sxs-lookup"><span data-stu-id="99048-393">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="99048-394">El código de llamada debe pasar un valor de la enumeración [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para el parámetro_contactInformationType_ _, que indica los datos que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="99048-394">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="99048-395">Al igual que el **GetContactInformation**, el método **BatchGetContactInformation** recupera varios elementos de presencia sobre el contacto desde el objeto **IContact** .</span><span class="sxs-lookup"><span data-stu-id="99048-395">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="99048-396">El código de llamada debe pasar en una matriz de valores de la enumeración **ContactInformationType** para el parámetro de_contactInformationTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="99048-396">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter.</span></span> <span data-ttu-id="99048-397">El método devuelve un objeto [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="99048-397">The method returns an [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="99048-398">La propiedad **IContact.Settings** devuelve un objeto **IContactSettingDictionary** que contiene propiedades personalizadas sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="99048-399">La propiedad **IContact.CustomGroups** devuelve un objeto **IGroupCollection** que incluye todos los grupos del que el contacto es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="99048-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="99048-400">Interfaz ISelf</span><span class="sxs-lookup"><span data-stu-id="99048-400">ISelf interface</span></span>
<span data-ttu-id="99048-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-401"></span></span>

<span data-ttu-id="99048-402">Durante el proceso de inicialización, la aplicación de Office obtiene los datos para el usuario actual mediante el acceso a la propiedad **ILyncClient.Self** , que debe devolver un objeto **ISelf** .</span><span class="sxs-lookup"><span data-stu-id="99048-402">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="99048-403">La interfaz **ISelf** representa el usuario de aplicación de cliente de mensajería instantánea local, ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="99048-403">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="99048-404">Tabla 6 se muestran a los miembros que deben implementarse en la clase que hereda de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="99048-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-405">Cualquier miembro de la interfaz de **ISelf** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-405">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-406">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-406">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="99048-407">**Tabla 6. Implementación de la interfaz de ISelf**</span><span class="sxs-lookup"><span data-stu-id="99048-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="99048-408">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-408">**Member**</span></span>|<span data-ttu-id="99048-409">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-410">**Contacto** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="99048-411">Obtiene el objeto **IContact** asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="99048-412">Presencia, modalidades disponibles, pertenencia a grupos y las propiedades de tipo de contacto para el usuario local se exponen a través de la propiedad **ISelf.Contact** (que devuelve un objeto **IContact** ).</span><span class="sxs-lookup"><span data-stu-id="99048-412">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="99048-413">Durante el proceso de inicialización, la aplicación de Office tiene acceso a la propiedad **ISelf.Contact** para obtener una referencia a la información de contacto para el usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-413">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="99048-414">Use el siguiente código para definir una clase que hereda de la interfaz **ISelf** que implementa la propiedad de **contacto** .</span><span class="sxs-lookup"><span data-stu-id="99048-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="99048-415">Interfaces de IContactManager y _IContactManagerEvents</span><span class="sxs-lookup"><span data-stu-id="99048-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="99048-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-416"></span></span>

<span data-ttu-id="99048-417">El objeto **IContactManager** administra los contactos del usuario local, incluida la información de contacto del usuario local propia.</span><span class="sxs-lookup"><span data-stu-id="99048-417">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="99048-418">La aplicación de Office, usa un objeto **IContactManager** para tener acceso a los objetos **IContact** que corresponden a los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-418">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="99048-419">Tabla 7 se muestran a los miembros que deben implementarse en la clase que hereda de **IContactManager** y **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="99048-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-420">Cualquier miembro de la interfaz de **IContactManager** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-421">Los miembros que están presentes, pero no implementado pueden producir una **NotImplementedException** o **E\_NOTIMPL** error.</span><span class="sxs-lookup"><span data-stu-id="99048-421">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="99048-422">Para obtener más información acerca de la **IContactManager** y **_IContactManagerEvents** interfaces y sus miembros, vea [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) y [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="99048-422">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="99048-423">**Tabla 7. Implementación de las interfaces IContactManager y _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="99048-424">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="99048-424">**Interface**</span></span>|<span data-ttu-id="99048-425">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-425">**Member**</span></span>|<span data-ttu-id="99048-426">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99048-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="99048-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="99048-428">**GetContactByUri** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="99048-429">Busca o crea una nueva instancia de contacto con el URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="99048-430">**CreateSubscription** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="99048-431">Crea un objeto **ISubscription** que se puede usar para el procesamiento por lotes suscripciones o consultas.</span><span class="sxs-lookup"><span data-stu-id="99048-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="99048-432">**Lookup** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="99048-433">Busca un contacto o grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="99048-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="99048-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="99048-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="99048-435">**OnGroupAdded** (evento)</span><span class="sxs-lookup"><span data-stu-id="99048-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="99048-436">Se produce cuando se agrega un grupo a una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="99048-436">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="99048-437">La colección de grupos actualizado puede obtenerse de la propiedad **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="99048-437">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="99048-438">**OnGroupRemoved** (evento)</span><span class="sxs-lookup"><span data-stu-id="99048-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="99048-439">Se produce cuando se quita un grupo de una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="99048-439">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="99048-440">La colección de grupos actualizado puede obtenerse de la propiedad **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="99048-440">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="99048-441">**OnSearchProviderStateChanged** (evento)</span><span class="sxs-lookup"><span data-stu-id="99048-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="99048-442">Se produce cuando cambia el estado de un proveedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="99048-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="99048-443">Office llama a **IContactManager.GetContactByUri** para obtener información de presencia de un contacto, mediante el uso de la dirección SIP del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-443">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="99048-444">Cuando un contacto está configurado para una dirección SIP en Active Directory, Office determina esta dirección para un contacto y las llamadas **GetContactByUri**, pasando la dirección SIP del contacto en el parámetro_contactUri_ _.</span><span class="sxs-lookup"><span data-stu-id="99048-444">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="99048-445">Cuando Office no puede determinar la dirección SIP del contacto, llama al método **IContactManager.Lookup** para encontrar el SIP mediante el servicio de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-445">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="99048-446">Aquí Office pasa los datos mejor que pueden encontrar el contacto (por ejemplo, la dirección de correo electrónico del contacto).</span><span class="sxs-lookup"><span data-stu-id="99048-446">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="99048-447">El método de **búsqueda** de forma asincrónica devuelve un objeto **AsynchronousOperation** .</span><span class="sxs-lookup"><span data-stu-id="99048-447">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="99048-448">Cuando invoca la devolución de llamada, el método de **búsqueda** debe devolver el éxito o el fracaso de la operación además del URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-448">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="99048-449">La aplicación de Office que se necesita para suscribirse a los cambios de presencia de un contacto individual.</span><span class="sxs-lookup"><span data-stu-id="99048-449">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="99048-450">Por lo tanto, cuando el estado de presencia de un contacto cambia, la aplicación de cliente de mensajería instantánea de las alertas del servidor de mensajería instantánea, con lo que las alertas a la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="99048-450">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="99048-451">Para ello, la aplicación de Office llama el método **IContactManager.CreateSubscription** para crear un nuevo objeto **IContactSubscription** para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="99048-451">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="99048-452">Interfaces de IGroup y IGroupCollection</span><span class="sxs-lookup"><span data-stu-id="99048-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="99048-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-453"></span></span>

<span data-ttu-id="99048-454">El objeto **IGroup** representa una colección de los contactos con propiedades adicionales para la identificación de la colección de contacto por un nombre de grupo colectiva.</span><span class="sxs-lookup"><span data-stu-id="99048-454">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="99048-455">Un objeto **IGroupCollection** representa una colección de objetos de **IGroup** definido por un usuario local y la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-455">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="99048-456">La aplicación de Office usa los objetos **IGroupCollection** y **IGroup** para tener acceso a los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="99048-456">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="99048-457">Tabla 9 se muestran a los miembros que deben implementarse en las clases que heredan de **IGroup** y **IGroupCollection** en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="99048-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="99048-458">Cualquier miembro de la interfaz de **IGroup** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-459">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="99048-460">Para obtener más información acerca de las interfaces **IGroup** y **IGroupCollection** y sus miembros, vea [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) y [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="99048-460">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="99048-461">**Tabla 9. Implementación de las interfaces IGroup y IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="99048-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="99048-462">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="99048-462">**Interface**</span></span>|<span data-ttu-id="99048-463">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-463">**Member**</span></span>|<span data-ttu-id="99048-464">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99048-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="99048-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="99048-466">**Count** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-466">**Count** property</span></span>  <br/> |<span data-ttu-id="99048-467">Devuelve el número de objetos de **IGroup** en la colección</span><span class="sxs-lookup"><span data-stu-id="99048-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="99048-468">**Elemento** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-468">**Item** property</span></span>  <br/> |<span data-ttu-id="99048-469">Devuelve el objeto **IGroup** en el índice especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="99048-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="99048-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="99048-470">**IGroup**</span></span> <br/> |<span data-ttu-id="99048-471">**ID** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-471">**Id** property</span></span>  <br/> |<span data-ttu-id="99048-472">Devuelve el identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="99048-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="99048-473">Cuando la aplicación de Office obtiene la información para el usuario local, que obtiene acceso a las pertenencias a grupos del contacto (usuario local) mediante una llamada a la propiedad **IContact.CustomGroups** , que devuelve un objeto **IGroupCollection** .</span><span class="sxs-lookup"><span data-stu-id="99048-473">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="99048-474">El **IGroupCollection** debe contener una matriz (o **lista**) de objetos de **IGroup** .</span><span class="sxs-lookup"><span data-stu-id="99048-474">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="99048-475">La clase que se deriva de **IGroupCollection** debe exponer una propiedad **Count** , que devuelve el número de elementos de la colección y un método de indizador, **this(int)**, que devuelve un objeto **IGroup** de la colección.</span><span class="sxs-lookup"><span data-stu-id="99048-475">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="99048-476">Interfaz IContactSubscription</span><span class="sxs-lookup"><span data-stu-id="99048-476">IContactSubscription interface</span></span>
<span data-ttu-id="99048-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-477"></span></span>

<span data-ttu-id="99048-478">La interfaz de **IContactSubscription** permite especificar los contactos para recibir actualizaciones de la información de presencia de y los tipos de información de presencia que desencadenan una notificación.</span><span class="sxs-lookup"><span data-stu-id="99048-478">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="99048-479">Aplicaciones de Office utilizan un objeto **IContactSubscription** para registrar los cambios realizados en el estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-479">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="99048-480">Tabla 10 se muestran a los miembros que deben implementarse en las clases que heredan de **IContactSubscription**.</span><span class="sxs-lookup"><span data-stu-id="99048-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-481">Cualquier miembro de la interfaz de **IContactSubscription** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-482">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="99048-483">Para obtener más información acerca de la interfaz de **IContactSubscription** y sus miembros, vea [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="99048-483">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="99048-484">**Tabla 10. Implementación de la interfaz de IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="99048-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="99048-485">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-485">**Member**</span></span>|<span data-ttu-id="99048-486">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-487">**AddContact** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="99048-488">Agrega un contacto para el objeto de suscripción.</span><span class="sxs-lookup"><span data-stu-id="99048-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="99048-489">**SUBSCRIBE** (método)</span><span class="sxs-lookup"><span data-stu-id="99048-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="99048-490">Ayuda a la aplicación de cliente de mensajería instantánea para supervisar la presencia de un contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="99048-491">La interfaz **IContactSubscription** debe contener una referencia a todos los objetos **IContact** que supervisa, utilizando una matriz o una **lista**.</span><span class="sxs-lookup"><span data-stu-id="99048-491">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="99048-492">El método **IContactSubscription.AddContact** agrega un objeto **IContact** para el a la estructura de datos subyacente del objeto **IContactSubscription** , con lo que se agrega un contacto nuevo para supervisar los cambios de presencia.</span><span class="sxs-lookup"><span data-stu-id="99048-492">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="99048-493">El método **IContactSubscription.Subscribe** permite que una aplicación de cliente de mensajería instantánea tener acceso a observadores de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-493">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="99048-494">Puede usar una estrategia de sondeo para obtener que la presencia desde el servidor para los contactos para que se ha suscrito a la aplicación de cliente de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="99048-494">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="99048-495">El método **Subscribe** es útil en situaciones donde se solicita la presencia de una persona ajena a la lista de contactos de un usuario (por ejemplo, de una red pública mayor).</span><span class="sxs-lookup"><span data-stu-id="99048-495">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="99048-496">Interfaz IContactEndPoint</span><span class="sxs-lookup"><span data-stu-id="99048-496">IContactEndPoint interface</span></span>
<span data-ttu-id="99048-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-497"></span></span>

<span data-ttu-id="99048-498">El **IContactEndPoint** representa un número de teléfono de colección de un contacto de números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="99048-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="99048-499">La tabla 11 se muestran a los miembros que deben implementarse en las clases que heredan de **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="99048-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-500">Cualquier miembro de la interfaz de **IContactEndPoint** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-501">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="99048-502">Para obtener más información acerca de la interfaz de **IContactEndPoint** y sus miembros, vea [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="99048-502">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="99048-503">**Tabla 11. Implementación de la interfaz de IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="99048-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="99048-504">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-504">**Member**</span></span>|<span data-ttu-id="99048-505">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-506">**DisplayName** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="99048-507">Obtiene la cadena para mostrar.</span><span class="sxs-lookup"><span data-stu-id="99048-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="99048-508">**Tipo** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-508">**Type** property</span></span>  <br/> |<span data-ttu-id="99048-509">Obtiene el tipo de contacto de extremo</span><span class="sxs-lookup"><span data-stu-id="99048-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="99048-510">**URI** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="99048-511">Obtiene el identificador URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="99048-512">Interfaz ILocaleString</span><span class="sxs-lookup"><span data-stu-id="99048-512">ILocaleString interface</span></span>
<span data-ttu-id="99048-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="99048-513"></span></span>

<span data-ttu-id="99048-514">El **ILocaleString** es una estructura de cadena localizada que contiene una cadena localizada y el identificador de configuración regional de la localización.</span><span class="sxs-lookup"><span data-stu-id="99048-514">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="99048-515">La interfaz de **ILocaleString** se usa para dar formato a la cadena de estado personalizado en la tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="99048-515">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="99048-516">La tabla 12 se muestran a los miembros que deben implementarse en las clases que heredan de **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="99048-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99048-517">Cualquier miembro de la interfaz de **ILocaleString** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="99048-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="99048-518">Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="99048-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="99048-519">Para obtener más información acerca de la interfaz de **ILocalString** y sus miembros, vea [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="99048-519">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="99048-520">**Tabla 12. Implementación de la interfaz de ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="99048-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="99048-521">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99048-521">**Member**</span></span>|<span data-ttu-id="99048-522">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99048-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99048-523">**LocaleId** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="99048-524">Obtiene el identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="99048-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="99048-525">**Valor** (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99048-525">**Value** property</span></span>  <br/> |<span data-ttu-id="99048-526">Obtiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="99048-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99048-527">Ver también</span><span class="sxs-lookup"><span data-stu-id="99048-527">See also</span></span>

- <span data-ttu-id="99048-528">Espacio de nombres [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="99048-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

