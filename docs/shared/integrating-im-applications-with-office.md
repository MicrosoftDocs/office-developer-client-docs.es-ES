---
title: Integración de aplicaciones de MI con Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013, como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.
localization_priority: Priority
ms.openlocfilehash: b3add86f011e016b1b6ea1a74f425f3f1deab002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700713"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="de85c-103">Integración de aplicaciones de MI con Office</span><span class="sxs-lookup"><span data-stu-id="de85c-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="de85c-104">Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013, como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="de85c-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="de85c-105">Si tienes alguna pregunta o comentarios sobre este artículo técnico o los procesos que describe, puedes ponerte en contacto con Microsoft enviando un correo a [docthis@microsoft.com](mailto:docthis@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="de85c-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="de85c-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="de85c-106">Introduction</span></span>
<span data-ttu-id="de85c-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-107"></span></span>

<span data-ttu-id="de85c-108">Office 2013 ofrece una completa integración con aplicaciones cliente de MI, incluida Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="de85c-108">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="de85c-109">Esta integración proporciona a los usuarios capacidades de MI desde dentro de Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 y OneNote 2013, así como la integración de presencia en las páginas de SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="de85c-109">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="de85c-110">Los usuarios pueden ver la foto, el nombre, el estado de presencia y los datos de contacto de los usuarios de su lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="de85c-110">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="de85c-111">Pueden iniciar una sesión de MI, realizar una videollamada o realizar una llamada telefónica directamente desde la tarjeta de contactos (el elemento de la IU en Office 2013 que expone opciones de información de contacto y comunicación).</span><span class="sxs-lookup"><span data-stu-id="de85c-111">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="de85c-112">Office 2013 te permite mantenerte conectado a tus contactos sin tener que salir de tus correos o documentos.</span><span class="sxs-lookup"><span data-stu-id="de85c-112">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="de85c-113">Este artículo usa el término aplicación cliente de MI para hacer referencia específicamente para la aplicación instalada en el equipo de un usuario que se comunica con el servicio de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-113">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="de85c-114">Por ejemplo, Lync 2013 se considera una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-114">For example, Lync 2013 is considered an IM client application.</span></span> <span data-ttu-id="de85c-115">Este artículo no proporciona detalles acerca de cómo se comunica la aplicación cliente de MI con el servicio de MI o acerca del servicio de MI en sí mismo.</span><span class="sxs-lookup"><span data-stu-id="de85c-115">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="de85c-116">Puedes personalizar una aplicación cliente de MI para que se comunique con Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-116">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="de85c-117">En concreto, puedes modificar la aplicación de MI para que muestre la siguiente información dentro de la IU de Office:</span><span class="sxs-lookup"><span data-stu-id="de85c-117">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="de85c-118">Foto del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-118">Contact photo.</span></span>
    
- <span data-ttu-id="de85c-119">Nombre de contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-119">Contact Name</span></span>
    
- <span data-ttu-id="de85c-120">Nota de estado personal del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="de85c-121">Estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-121">Contact presence status.</span></span>
    
- <span data-ttu-id="de85c-122">Cadena de disponibilidad del contacto (por ejemplo, "Disponible" o "Fuera de la oficina").</span><span class="sxs-lookup"><span data-stu-id="de85c-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="de85c-123">Cadena de función del contacto (por ejemplo, "listo para video").</span><span class="sxs-lookup"><span data-stu-id="de85c-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="de85c-124">Inicio de MI con un solo clic.</span><span class="sxs-lookup"><span data-stu-id="de85c-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="de85c-125">Inicio de videollamada con un solo clic.</span><span class="sxs-lookup"><span data-stu-id="de85c-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="de85c-126">Inicio de llamada de teléfono con un solo clic (incluye SIP, número de teléfono, correo de voz y llamada a un número nuevo).</span><span class="sxs-lookup"><span data-stu-id="de85c-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="de85c-127">Administración de contactos (agregar al grupo de MI).</span><span class="sxs-lookup"><span data-stu-id="de85c-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="de85c-128">Ubicación y zona horaria del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="de85c-129">Datos, número de teléfono, dirección de correo, puesto y nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="de85c-130">**Ilustración 1. Tarjeta de contactos en Office 2013**</span><span class="sxs-lookup"><span data-stu-id="de85c-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="de85c-131">![Tarjeta de contactos en Office 2013](media/ocom15_peoplecard.png "Tarjeta de contactos en Office 2013")</span><span class="sxs-lookup"><span data-stu-id="de85c-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="de85c-132">Para habilitar la integración con Office, una aplicación cliente de MI debe implementar un conjunto de interfaces de conexión que proporciona Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-132">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="de85c-133">Se incluyen las API para esta integración en el espacio de nombre [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) contenido en el archivo Microsoft.Office.UC.dll, que se instala con las versiones de Office 2013 que incluyen Lync o Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="de85c-133">The APIs for this integration are included in the [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="de85c-134">El espacio de nombre **UCCollaborationLib** incluye las interfaces que debes implementar para la integración con Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-134">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="de85c-135">La biblioteca de tipos para las interfaces necesarias está incrustada en Lync 2013 o Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="de85c-135">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="de85c-136">Para integradores de terceros, esto solo funciona cuando los equipos de destino tienen instalado Lync 2013 y en Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="de85c-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="de85c-137">Si realizas la integración con Office Standard, deberás extraer la biblioteca de tipos e instalarla en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="de85c-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="de85c-138">El [SDK de Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) incluye el archivo Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="de85c-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="de85c-139">Algunas aplicaciones de Office 2010 puede integrarse de forma similar con una aplicación de proveedores de MI de terceros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 y SharePoint Server 2010 (con un control ActiveX).</span><span class="sxs-lookup"><span data-stu-id="de85c-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="de85c-140">Muchos de los pasos necesarios para la integración con Office 2013 se aplican también a Office 2010.</span><span class="sxs-lookup"><span data-stu-id="de85c-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="de85c-141">Hay varias diferencias clave en la forma en la que Office 2010 se integra con una aplicación de proveedor de MI:</span><span class="sxs-lookup"><span data-stu-id="de85c-141">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="de85c-142">Office 2010 no muestra la foto del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-142">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="de85c-143">Debes descargar el archivo Microsoft.Office.Uc.dll por separado de Office 2010.</span><span class="sxs-lookup"><span data-stu-id="de85c-143">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="de85c-144">El [SDK de Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) incluye el archivo Microsoft.Office.UC.dll para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="de85c-144">The [Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="de85c-145">Cuando la aplicación de Office llama al método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) en la aplicación cliente de MI, pasa la cadena "14.0.0.0".</span><span class="sxs-lookup"><span data-stu-id="de85c-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="de85c-146">Office 2010 enumera todos los grupos y contactos en cuanto se conecta a una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-146">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="de85c-147">Integración de Office con una aplicación cliente de MI</span><span class="sxs-lookup"><span data-stu-id="de85c-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="de85c-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-148"></span></span>

<span data-ttu-id="de85c-149">Cuando se inicia una aplicación de Office 2013, atraviesa el siguiente proceso para integrarse con la aplicación cliente de MI predeterminada:</span><span class="sxs-lookup"><span data-stu-id="de85c-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="de85c-150">Comprueba el registro para descubrir la aplicación cliente de MI predeterminada y, a continuación, se conecta a ella.</span><span class="sxs-lookup"><span data-stu-id="de85c-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="de85c-151">Se autentica con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="de85c-152">Se conecta a interfaces específicas expuestas por la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="de85c-153">Determina las funciones del usuario que inició sesión actualmente (usuario local), incluida la obtención de los contactos del usuario, la determinación de la presencia del usuario y la determinación de las capacidades de MI del usuario (mensajería instantánea, chat de video, VOIP, etc.).</span><span class="sxs-lookup"><span data-stu-id="de85c-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="de85c-154">Obtiene la información de presencia de los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="de85c-155">Cuando se cierra la aplicación cliente de MI, la aplicación de Office 2013 se desconecta de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="de85c-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="de85c-156">Descubrir la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="de85c-156">Discovering the IM application</span></span>

<span data-ttu-id="de85c-157">La aplicación de Office busca varias teclas y entradas específicas en el registro para obtener información sobre la aplicación cliente de MI de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="de85c-157">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="de85c-158">Si detecta una aplicación cliente de MI de forma predeterminada, a continuación, intenta conectarse a ella.</span><span class="sxs-lookup"><span data-stu-id="de85c-158">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="de85c-159">El proceso que realiza la aplicación de Office para obtener información sobre la aplicación cliente de MI predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="de85c-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="de85c-160">La aplicación de Office intenta ver si se establece la subclave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp en el registro y lee el nombre de aplicación que aparece allí.</span><span class="sxs-lookup"><span data-stu-id="de85c-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="de85c-161">La aplicación de Office, a continuación, lee la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning y controla el valor para detectar cambios.</span><span class="sxs-lookup"><span data-stu-id="de85c-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="de85c-162">La aplicación de Office a continuación lee la clave del registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ y obtiene los valores de ProcessName e identificador de clase (CLSID) almacenados allí.</span><span class="sxs-lookup"><span data-stu-id="de85c-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="de85c-163">Una vez que la aplicación cliente de MI completó correctamente su secuencia de inicio y registró todas las clases correctamente para la integración de presencia, establece la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning en "2", lo que indica que se está ejecutando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="de85c-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="de85c-164">Cuando la aplicación de Office detecta que la clave de HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning se estableció en "2", comprueba la lista de procesos en ejecución en el equipo para ver el nombre de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="de85c-165">Una vez que la aplicación de Office encuentra el proceso que utiliza la aplicación cliente de MI, la aplicación de Office llama a **CoCreateInstance** mediante CLSID para establecer una conexión con la aplicación cliente de MI como servidor COM fuera del proceso.</span><span class="sxs-lookup"><span data-stu-id="de85c-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="de85c-166">Autenticación de la conexión a la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="de85c-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="de85c-167">Después de que la aplicación de Office establece una conexión con la aplicación cliente de MI, a continuación, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="de85c-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="de85c-168">La aplicación de Office llama al método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para comprobar la interfaz [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="de85c-168">The Office application calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="de85c-169">La aplicación de Office, a continuación, llama al método **IUCOfficeIntegration.GetAuthenticationInfo**, pasando la versión más alta de integración compatible (por ejemplo, "15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="de85c-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="de85c-170">Si la aplicación cliente de MI es compatible con la versión de Office que se pasa como un parámetro, la aplicación devuelve la siguiente cadena XML codificada de forma rígida al código de llamada:</span><span class="sxs-lookup"><span data-stu-id="de85c-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="de85c-171">Por motivos heredados, la aplicación cliente de MI debe devolver el valor exacto `<authenticationinfo>` a la llamada a **GetAuthenticationInfo** si se admite la versión de Office pasado como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="de85c-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="de85c-172">Si la aplicación cliente no puede devolver un valor, la aplicación de Office llama al método **GetAuthenticationInfo** nuevamente con la siguiente versión más alta compatible de Office (por ejemplo, "14.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="de85c-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="de85c-173">Cuando Office determina que la aplicación cliente de MI es compatible con la integración de presencia y MI, se conecta a un conjunto requerido de interfaces para finalizar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="de85c-173">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="de85c-174">(Para obtener más información, consulta [Conectarse a interfaces necesarias](#off15_IMIntegration_HowConnect).)</span><span class="sxs-lookup"><span data-stu-id="de85c-174">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="de85c-175">Si la aplicación de Office, produce un error en cualquiera de los pasos anteriores, retrocede y no se establece la integración de presencia durante la sesión de la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="de85c-176">Conexión a las interfaces necesarias</span><span class="sxs-lookup"><span data-stu-id="de85c-176">Connecting to required interfaces</span></span>
<span data-ttu-id="de85c-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-177"></span></span>

<span data-ttu-id="de85c-178">Después de autenticar la conexión a la aplicación cliente de MI, la aplicación de Office intenta conectarse a un conjunto de interfaces necesarias que debe exponer la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-178">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="de85c-179">La aplicación de Office lo logra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="de85c-179">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="de85c-180">La aplicación de Office obtiene un objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceLyncClient** desde la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="de85c-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="de85c-181">La aplicación de Office obtiene un objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceAutomation** desde la enumeración **OIInterface**.</span><span class="sxs-lookup"><span data-stu-id="de85c-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="de85c-182">La aplicación de Office configura la escucha de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient).</span><span class="sxs-lookup"><span data-stu-id="de85c-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="de85c-183">La aplicación de Office, configura la escucha de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="de85c-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="de85c-184">La aplicación de Office obtiene el estado de inicio de sesión de la aplicación cliente de MI mediante el acceso a la propiedad **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="de85c-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="de85c-185">La aplicación de Office obtiene las capacidades de la aplicación cliente de MI al llamar al método **IUCOfficeIntegration.GetSupportedFeatures**, que devuelve una marca de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="de85c-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="de85c-186">La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Self** para obtener una referencia a un objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="de85c-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="de85c-187">Recuperar las capacidades del usuario local</span><span class="sxs-lookup"><span data-stu-id="de85c-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="de85c-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-188"></span></span>

<span data-ttu-id="de85c-189">La aplicación de Office obtiene las capacidades del usuario local mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="de85c-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="de85c-190">Si la aplicación cliente de MI es compatible con la interfaz **IClient2**, Office intenta obtener un objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) mediante el acceso a la propiedad **IClient2.PrivateContactManager**.</span><span class="sxs-lookup"><span data-stu-id="de85c-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="de85c-191">Si la aplicación de MI no es compatible con la interfaz **IClient2**, la aplicación de Office intenta obtener un objeto **IContactManager** mediante el acceso a la propiedad **ILyncClient.ContactManager**.</span><span class="sxs-lookup"><span data-stu-id="de85c-191">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="de85c-192">La aplicación cliente de MI debe devolver correctamente un objeto **IContactManager** antes de que se puedan establecer otras capacidades de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-192">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="de85c-193">La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Uri** y después llama a **IContactManager.GetContactByUri** para obtener el objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="de85c-194">A continuación, la aplicación de Office hace varias llamadas a **IContact.CanStart** para establecer las capacidades del usuario local, al pasar los valores de **ModalityTypes.ucModalityInstantMessage** y \*\* ModalityTypes.ucModalityAudioVideo\*\* sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="de85c-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="de85c-195">Recuperar presencia de contactos</span><span class="sxs-lookup"><span data-stu-id="de85c-195">Retrieving contact presence</span></span>
<span data-ttu-id="de85c-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-196"></span></span>

<span data-ttu-id="de85c-197">La aplicación de Office obtiene la presencia de contactos, incluido el usuario local, mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="de85c-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="de85c-198">La aplicación de Office llama a **IContact.GetContactInformation** para obtener un elemento de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="de85c-199">A continuación, la aplicación de Office se suscribe a los cambios de estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-199">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="de85c-200">Llama a **IContactManager.CreateSubscription** para obtener un objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="de85c-200">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="de85c-201">A continuación, llama a **IContactSubscription.AddContact** para agregar el contacto a la suscripción y luego llama a **IContactSubscription.Subscribe** para obtener los cambios de estado del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-201">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="de85c-202">Si la aplicación de MI es compatible con **IContact2**, Office intenta obtener información de presencia llamando a **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="de85c-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="de85c-203">A continuación, la aplicación de Office recupera las propiedades de la presencia del contacto llamando a **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="de85c-203">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="de85c-204">La aplicación de Office puede obtener un segundo conjunto de propiedades de presencia si obtiene acceso a la propiedad **IContact.Settings**.</span><span class="sxs-lookup"><span data-stu-id="de85c-204">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="de85c-205">Por último, la aplicación de Office obtiene la pertenencia del grupo del contacto al acceder a la propiedad **IContact.CustomGroups**.</span><span class="sxs-lookup"><span data-stu-id="de85c-205">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="de85c-206">Esto le devuelve una colección [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que incluye a todos los objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) a los que pertenece el contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-206">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="de85c-207">Desconexión de la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="de85c-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="de85c-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-208"></span></span>

<span data-ttu-id="de85c-209">Cuando la aplicación de Office 2013 detecta el evento **OnShuttingDown** desde la aplicación de MI, se desconecta silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="de85c-209">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="de85c-210">Sin embargo, si cierra la aplicación de Office antes de la aplicación de MI, la aplicación de Office no garantiza que la conexión se limpie.</span><span class="sxs-lookup"><span data-stu-id="de85c-210">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="de85c-211">La aplicación de MI debe controlar pérdidas de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="de85c-211">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="de85c-212">Entradas y claves del registro de configuración</span><span class="sxs-lookup"><span data-stu-id="de85c-212">Setting registry keys and entries</span></span>
<span data-ttu-id="de85c-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-213"></span></span>

<span data-ttu-id="de85c-214">Como se indicó anteriormente, las aplicaciones de Office 2013 compatibles con MI buscan teclas, entradas y valores específicos en el registro para obtener información sobre la aplicación cliente de MI a la cual conectarse.</span><span class="sxs-lookup"><span data-stu-id="de85c-214">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="de85c-215">Estos valores de registro le proporcionan a la aplicación de Office el nombre del proceso y CLSID de la clase que actúa como punto de entrada al modelo de objeto de la aplicación cliente de MI (es decir, la clase que implementa la interfaz **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="de85c-215">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="de85c-216">La aplicación de Office crea conjuntamente la clase y se conecta como cliente al servidor COM fuera de proceso en la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-216">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="de85c-217">Usa la tabla 1 para identificar las claves, entradas y valores que deben escribirse en el registro para integrar una aplicación cliente de MI con Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="de85c-218">**Tabla 1. Claves del registro para configurar la aplicación cliente de MI predeterminada**</span><span class="sxs-lookup"><span data-stu-id="de85c-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="de85c-219">**Clave**</span><span class="sxs-lookup"><span data-stu-id="de85c-219">**Key**</span></span>|<span data-ttu-id="de85c-220">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="de85c-220">**Entry**</span></span>|<span data-ttu-id="de85c-221">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="de85c-221">**Type**</span></span>|<span data-ttu-id="de85c-222">**Valor**</span><span class="sxs-lookup"><span data-stu-id="de85c-222">**Value**</span></span>|<span data-ttu-id="de85c-223">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="de85c-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="de85c-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span><span class="sxs-lookup"><span data-stu-id="de85c-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="de85c-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="de85c-225">FriendlyName element</span></span>  <br/> |<span data-ttu-id="de85c-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="de85c-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="de85c-227">El nombre de la aplicación cliente de MI de terceros.</span><span class="sxs-lookup"><span data-stu-id="de85c-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="de85c-228">MI de Litware 2012</span><span class="sxs-lookup"><span data-stu-id="de85c-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="de85c-229">ProcessName</span><span class="sxs-lookup"><span data-stu-id="de85c-229">ProcessName</span></span>  <br/> |<span data-ttu-id="de85c-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="de85c-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="de85c-231">El nombre del proceso de la aplicación cliente de MI de terceros.</span><span class="sxs-lookup"><span data-stu-id="de85c-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="de85c-232">litware.exe</span><span class="sxs-lookup"><span data-stu-id="de85c-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="de85c-233">GUID</span><span class="sxs-lookup"><span data-stu-id="de85c-233">GUID</span></span>  <br/> |<span data-ttu-id="de85c-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="de85c-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="de85c-235">Un identificador de clase (CLSID) para la clase de creación conjunta de raíz en la aplicación de MI (la clase que implementa la interfaz **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="de85c-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="de85c-236">(Un GUID)</span><span class="sxs-lookup"><span data-stu-id="de85c-236">A GUID.</span></span>  <br/> |
|<span data-ttu-id="de85c-237">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="de85c-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="de85c-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="de85c-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="de85c-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="de85c-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="de85c-240">El nombre de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-240">The name of the application.</span></span> <span data-ttu-id="de85c-241">Debe ser el mismo que el nombre de la clave del registro de nivel superior (subárbol) en HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="de85c-241">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="de85c-242">Litware</span><span class="sxs-lookup"><span data-stu-id="de85c-242">Litware</span></span>  <br/> |
|<span data-ttu-id="de85c-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span><span class="sxs-lookup"><span data-stu-id="de85c-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="de85c-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="de85c-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="de85c-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="de85c-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="de85c-246">Valor entero entre 0 y 2:</span><span class="sxs-lookup"><span data-stu-id="de85c-246">An integer value between 0 and 255.</span></span>  <br/>  <span data-ttu-id="de85c-247">0—No en ejecución</span><span class="sxs-lookup"><span data-stu-id="de85c-247">0—Not running</span></span>  <br/>  <span data-ttu-id="de85c-248">1—Iniciándose</span><span class="sxs-lookup"><span data-stu-id="de85c-248">1—Starting</span></span>  <br/>  <span data-ttu-id="de85c-249">2—En ejecución</span><span class="sxs-lookup"><span data-stu-id="de85c-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="de85c-250">**NOTA**: la clave del registro de nombre de aplicación debe ser igual al valor de la entrada DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="de85c-250">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="de85c-251">Implementar las interfaces necesarias para la integración con Office</span><span class="sxs-lookup"><span data-stu-id="de85c-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="de85c-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-252"></span></span>

<span data-ttu-id="de85c-253">Hay tres interfaces del espacio de nombre **UCCollaborationLib** que debe implementar el archivo ejecutable (o servidor COM) de una aplicación cliente de MI para que se pueda integrar con Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-253">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="de85c-254">Si no se implementan estas interfaces, la aplicación de Office retrocede durante el proceso de inicialización y no se establece la conexión con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-254">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="de85c-255">Las interfaces necesarias son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="de85c-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="de85c-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). Si bien no es necesaria, la interfaz **_IUCOfficeIntegrationEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="de85c-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="de85c-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). Si bien no es necesaria, la interfaz **_ILyncClientEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="de85c-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="de85c-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="de85c-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="de85c-259">Interfaz IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="de85c-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="de85c-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-260"></span></span>

<span data-ttu-id="de85c-261">La interfaz **IUCOfficeIntegration** proporciona el punto de entrada para que una aplicación de Office se conecte a la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-261">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="de85c-262">La interfaz define tres métodos que una aplicación de Office llama como parte del proceso de iniciar una conexión con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-262">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="de85c-263">La clase que implementa la interfaz **IUCOfficeIntegration** se debe poder cocrear para que Office pueda cocrear una instancia de ella.</span><span class="sxs-lookup"><span data-stu-id="de85c-263">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="de85c-264">Además, debe exponer la CLSID que se introduce como el valor de la entrada de GUID en la clave de registro HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_</span><span class="sxs-lookup"><span data-stu-id="de85c-264">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="de85c-265">La clase que hereda de **IUCOfficeIntegration** también debe implementar la interfaz **_IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="de85c-265">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="de85c-266">La interfaz **_IUCOfficeIntegrationEvents** contiene los miembros que exponen los controladores de eventos de la interfaz **IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="de85c-266">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="de85c-267">La Tabla 2 muestra los miembros que deben implementarse en la clase que hereda de **IUCOfficeIntegration** y **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="de85c-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-268">Para más información sobre las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegrationEvents** y sus miembros, consulta [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) y [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="de85c-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="de85c-269">**Tabla 2. Implementación de las interfaces IUCOfficeIntegration y _IUCOfficeIntegrationEvents interfaces**</span><span class="sxs-lookup"><span data-stu-id="de85c-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="de85c-270">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="de85c-270">**Interface**</span></span>|<span data-ttu-id="de85c-271">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-271">**Member**</span></span>|<span data-ttu-id="de85c-272">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de85c-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="de85c-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="de85c-274">Método **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="de85c-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="de85c-275">Obtiene la cadena de información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="de85c-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="de85c-276">Método **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="de85c-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="de85c-277">Obtiene la interfaz de una versión específica.</span><span class="sxs-lookup"><span data-stu-id="de85c-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="de85c-278">Método **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="de85c-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="de85c-279">Obtiene las características de integración de Office compatibles.</span><span class="sxs-lookup"><span data-stu-id="de85c-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="de85c-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="de85c-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="de85c-281">Evento **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="de85c-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="de85c-282">El evento que se produce cuando la aplicación cliente de MI está intentando cerrarse.</span><span class="sxs-lookup"><span data-stu-id="de85c-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="de85c-283">Usa el código siguiente para definir una clase que herede de las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegration** dentro de una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
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

<span data-ttu-id="de85c-284">El método **GetAuthenticationInfo** toma una cadena como argumento para el parámetro _version_.</span><span class="sxs-lookup"><span data-stu-id="de85c-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="de85c-285">Cuando la aplicación de Office llama a este método, pasa una de las dos cadenas del argumento, según la versión de Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="de85c-286">Cuando la aplicación de Office proporciona el método con la versión de Office compatible con la aplicación cliente de MI (es decir, compatible con la funcionalidad), el método **GetAuthenticationInfo** devuelve una cadena XML codificada de forma rígida `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="de85c-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="de85c-287">Usa el código siguiente para implementar un método **GetAuthentication** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="de85c-288">El método **GetInterface** envía las referencias a clases al código de llamada, dependiendo de lo que se pasa como argumento para el parámetro de la _interface_.</span><span class="sxs-lookup"><span data-stu-id="de85c-288">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="de85c-289">Cuando una aplicación de Office llama al método **GetInterface**, pasa uno de los dos valores para el parámetro de la interfaz: la constante **oiInterfaceILyncClient** (1) o \*\* la constante oiInterfaceIAutomation\*\* (2) de la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="de85c-289">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="de85c-290">Si la aplicación de Office pasa la constante **oiInterfaceILyncClient**, el método **GetInterface** devuelve una referencia a una clase que implementa la interfaz **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="de85c-290">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="de85c-291">Si la aplicación de Office pasa la constante **oiInterfaceIAutomation**, el método **GetInterface** devuelve una clase que implementa la interfaz **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="de85c-291">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="de85c-292">Usa el siguiente código de ejemplo para implementar el método **GetInterface** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="de85c-293">El método **GetSupportedFeatures** devuelve información sobre las características de MI compatibles con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-293">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="de85c-294">Es necesaria una cadena para el único parámetro, _version_.</span><span class="sxs-lookup"><span data-stu-id="de85c-294">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="de85c-295">Cuando la aplicación de Office llama al método **GetSupportFeatures**, el método devuelve un valor de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="de85c-295">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="de85c-296">El valor devuelto especifica las capacidades del cliente de MI, donde cada función de la aplicación cliente de MI se indica en la aplicación de Office mediante la adición de un marcador al valor.</span><span class="sxs-lookup"><span data-stu-id="de85c-296">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="de85c-297">Las aplicaciones de Office 2013 ignoran las siguientes constantes en la enumeración**OIFeature**:</span><span class="sxs-lookup"><span data-stu-id="de85c-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="de85c-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="de85c-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="de85c-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="de85c-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="de85c-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="de85c-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="de85c-301">Usa el siguiente código de ejemplo para implementar el método **GetSupportFeatures** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="de85c-302">Interfaz ILyncClient</span><span class="sxs-lookup"><span data-stu-id="de85c-302">ILyncClient interface</span></span>
<span data-ttu-id="de85c-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-303"></span></span>

<span data-ttu-id="de85c-304">La interfaz **ILyncClient** se aplica a las funcionalidades de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-304">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="de85c-305">Expone propiedades que hacen referencia a la persona que inició sesión en la aplicación (usuario local, representado por la interfaz [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), el estado de la aplicación, la lista de contactos del usuario local y otras configuraciones.</span><span class="sxs-lookup"><span data-stu-id="de85c-305">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="de85c-306">Cuando está intentando conectarse a la aplicación cliente de MI, la aplicación de Office obtiene una referencia a un objeto que implementa la interfaz **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="de85c-306">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="de85c-307">Desde esa referencia, Office puede acceder a muchas de las funciones de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-307">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="de85c-308">Además, la clase que implementa la interfaz **ILyncClient** también debe implementar la interfaz **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="de85c-308">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="de85c-309">La interfaz **_ILyncClientEvents** expone muchos de los eventos que son necesarios para supervisar el estado de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-309">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="de85c-310">La Tabla 3 muestra los miembros que deben implementarse en la clase que hereda de **ILyncClient** y **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="de85c-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-311">Cualquier miembro de la interfaz **ILyncClient** o \*\* \_ILyncClientEvents\*\* que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-311">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-312">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-312">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="de85c-313">Para más información sobre las interfaces **ILyncClient** y **_ILyncClientEvents** y sus miembros, consulta [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) y [ UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="de85c-313">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="de85c-314">**Tabla 3. Implementación de interfaces ILyncClient e ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="de85c-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="de85c-315">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="de85c-315">**Interface**</span></span>|<span data-ttu-id="de85c-316">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-316">**Member**</span></span>|<span data-ttu-id="de85c-317">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de85c-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="de85c-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="de85c-319">Propiedad **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="de85c-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="de85c-320">Obtiene el administrador de grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="de85c-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="de85c-321">Propiedad **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="de85c-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="de85c-322">Obtiene el administrador de conversación.</span><span class="sxs-lookup"><span data-stu-id="de85c-322">Gets the user's manager.</span></span>  <br/> |
||<span data-ttu-id="de85c-323">Propiedad **Self**</span><span class="sxs-lookup"><span data-stu-id="de85c-323">**Self** property</span></span>  <br/> |<span data-ttu-id="de85c-324">Obtiene el objeto **Self**.</span><span class="sxs-lookup"><span data-stu-id="de85c-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="de85c-325">Método **SignIn**</span><span class="sxs-lookup"><span data-stu-id="de85c-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="de85c-326">Inicia el proceso de inicio de sesión de la aplicación cliente de MI con una disponibilidad específica.</span><span class="sxs-lookup"><span data-stu-id="de85c-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="de85c-327">Propiedad **State**</span><span class="sxs-lookup"><span data-stu-id="de85c-327">State property</span></span>  <br/> |<span data-ttu-id="de85c-328">Obtiene el estado actual de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="de85c-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="de85c-329">Propiedad **Uri**</span><span class="sxs-lookup"><span data-stu-id="de85c-329">**Uri Property**</span></span>  <br/> |<span data-ttu-id="de85c-330">Obtiene el URI de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="de85c-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="de85c-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="de85c-332">Evento **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="de85c-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="de85c-333">Se produce cuando cambia el estado de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-333">Raised when the IM client application state changes.</span></span> <span data-ttu-id="de85c-334">Debes controlar este evento y obtener la propiedad **eventData.NewState**.</span><span class="sxs-lookup"><span data-stu-id="de85c-334">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="de85c-335">Se produce el evento para todos los procesos vinculados a una instancia de una aplicación cliente de MI cuando cualquier subsistema de la aplicación hace que cambie el estado.</span><span class="sxs-lookup"><span data-stu-id="de85c-335">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="de85c-336">Durante el proceso de inicialización, Office obtiene acceso a la propiedad **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="de85c-336">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="de85c-337">Esta propiedad debe devolver un valor de la enumeración [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState).</span><span class="sxs-lookup"><span data-stu-id="de85c-337">This property needs to return a value from the [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
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

<span data-ttu-id="de85c-338">La propiedad **State** almacena el estado actual de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-338">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="de85c-339">Se debe establecer y actualizar durante la sesión de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-339">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="de85c-340">Cuando la aplicación cliente de MI inicia sesión, cierra sesión o se apaga, debe establecer la propiedad **State**.</span><span class="sxs-lookup"><span data-stu-id="de85c-340">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="de85c-341">Es mejor establecer esta propiedad dentro de los métodos **ILyncClient.SignIn** y **ILyncClient.SignOut**, como demuestra el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="de85c-341">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
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

<span data-ttu-id="de85c-342">En el siguiente ejemplo de código se muestra cómo configurar la escucha de eventos con las interfaces _ **ILyncClientEvents** y _ **IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="de85c-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
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

### <a name="iautomation-interface"></a><span data-ttu-id="de85c-343">Interfaz IAutomation</span><span class="sxs-lookup"><span data-stu-id="de85c-343">IAutomation interface</span></span>
<span data-ttu-id="de85c-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-344"></span></span>

<span data-ttu-id="de85c-345">La interfaz **IAutomation** automatiza características de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-345">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="de85c-346">Puedes usarla para iniciar conversaciones, unirte a conferencias y proporcionar contexto de la ventana de extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="de85c-346">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="de85c-347">La Tabla 4 muestra los miembros que deben implementarse en la clase que hereda de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="de85c-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-348">Cualquier miembro de la interfaz **IAutomation**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-349">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="de85c-350">Para más información sobre la interfaz **IAutomation** y sus miembros, consulta [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="de85c-350">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="de85c-351">**Tabla 4. Implementación de interfaz IAutomation**</span><span class="sxs-lookup"><span data-stu-id="de85c-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="de85c-352">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-352">**Member**</span></span>|<span data-ttu-id="de85c-353">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-354">Método **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="de85c-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="de85c-355">Inicia una conversación con la modalidad de conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="de85c-355">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="de85c-356">Se devuelve una instancia de **IConversationWindow**.</span><span class="sxs-lookup"><span data-stu-id="de85c-356">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="de85c-357">Implementar la integración de presencia de los contactos</span><span class="sxs-lookup"><span data-stu-id="de85c-357">Implementing contact presence integration</span></span>
<span data-ttu-id="de85c-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-358"></span></span>

<span data-ttu-id="de85c-359">Además de las tres interfaces necesarias descritas anteriormente, hay varias otras interfaces que son importantes para habilitar la funcionalidad de presencia de los contactos en Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-359">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="de85c-360">Entre ellas se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="de85c-360">These members include the following properties:</span></span>
  
- <span data-ttu-id="de85c-361">La interfaz de [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) o **IContact2**.</span><span class="sxs-lookup"><span data-stu-id="de85c-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="de85c-362">La interfaz [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="de85c-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="de85c-363">Las interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) y [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager).</span><span class="sxs-lookup"><span data-stu-id="de85c-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="de85c-364">Las interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) y [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup).</span><span class="sxs-lookup"><span data-stu-id="de85c-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="de85c-365">La interfaz [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="de85c-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="de85c-366">La interfaz [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint).</span><span class="sxs-lookup"><span data-stu-id="de85c-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="de85c-367">La interfaz [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="de85c-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="de85c-368">Interfaz IContact</span><span class="sxs-lookup"><span data-stu-id="de85c-368">IContact interface</span></span>
<span data-ttu-id="de85c-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-369"></span></span>

<span data-ttu-id="de85c-370">La interfaz **IContact** representa un usuario de una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-370">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="de85c-371">La interfaz expone propiedades de presencia, modalidades disponibles, pertenencia a un grupo y tipo de contacto para un usuario.</span><span class="sxs-lookup"><span data-stu-id="de85c-371">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="de85c-372">Para iniciar una conversación con otro usuario, necesitas especificar esa instancia de usuario de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="de85c-372">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="de85c-373">La Tabla 5 muestra los miembros que deben implementarse en la clase que hereda de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="de85c-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-374">Cualquier miembro de la interfaz **IContact**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-375">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="de85c-376">Para más información sobre la interfaz **IContact** y sus miembros, consulta [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="de85c-376">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="de85c-377">**Tabla 5. Implementación de interfaz IContact**</span><span class="sxs-lookup"><span data-stu-id="de85c-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="de85c-378">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-378">**Member**</span></span>|<span data-ttu-id="de85c-379">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-380">Método **CanStart**</span><span class="sxs-lookup"><span data-stu-id="de85c-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="de85c-381">Devuelve **true** si se puede iniciar un determinado tipo de modalidad en el contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="de85c-382">Método **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="de85c-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="de85c-383">Obtiene un elemento de la presencia de un contacto de publicación.</span><span class="sxs-lookup"><span data-stu-id="de85c-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="de85c-384">Método **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="de85c-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="de85c-385">Obtiene un elemento de presencia de un contacto de publicación.</span><span class="sxs-lookup"><span data-stu-id="de85c-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="de85c-386">Propiedad **Configuración**</span><span class="sxs-lookup"><span data-stu-id="de85c-386">**Settings Property**</span></span>  <br/> |<span data-ttu-id="de85c-387">Obtiene una colección de propiedades del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="de85c-388">Propiedad **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="de85c-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="de85c-389">Obtiene una colección de grupos de los que el contacto es miembro.</span><span class="sxs-lookup"><span data-stu-id="de85c-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="de85c-390">Durante el proceso de inicialización, la aplicación de Office llama al método **IContact.CanStart** para determinar las funcionalidades de MI para el usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-390">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="de85c-391">El método **CanStart** toma una marca de la enumeración [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como argumento para el parámetro __modalityTypes_.</span><span class="sxs-lookup"><span data-stu-id="de85c-391">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter.</span></span> <span data-ttu-id="de85c-392">Si el usuario actual puede participar en la modalidad solicitada (es decir, el usuario puede utilizar mensajería instantánea, mensajes de audio y video y uso compartido de aplicaciones), el método **CanStart** devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="de85c-392">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
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

<span data-ttu-id="de85c-393">El método **GetContactInformation** recupera información sobre el contacto del objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="de85c-393">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="de85c-394">El código de llamada debe pasar un valor de la enumeración [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para el parámetro __contactInformationType_, que indica los datos que se deben recuperar.</span><span class="sxs-lookup"><span data-stu-id="de85c-394">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
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

<span data-ttu-id="de85c-395">Similar al método **GetContactInformation**, el método **BatchGetContactInformation** recupera varios elementos de presencia sobre el contacto del objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="de85c-395">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="de85c-396">El código de llamada debe pasar de una matriz de valores de la enumeración **ContactInformationType** para el parámetro __contactInformationTypes_.</span><span class="sxs-lookup"><span data-stu-id="de85c-396">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter.</span></span> <span data-ttu-id="de85c-397">El método devuelve un objeto [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="de85c-397">The method returns an [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
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

<span data-ttu-id="de85c-398">La propiedad **IContact.Settings** devuelve un objeto **IContactSettingDictionary** que contiene las propiedades personalizadas sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
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

<span data-ttu-id="de85c-399">La propiedad **IContact.CustomGroups** devuelve un objeto **IGroupCollection** que incluye todos los grupos de los que el contacto es miembro.</span><span class="sxs-lookup"><span data-stu-id="de85c-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
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

### <a name="iself-interface"></a><span data-ttu-id="de85c-400">Interfaz ISelf</span><span class="sxs-lookup"><span data-stu-id="de85c-400">ISelf interface</span></span>
<span data-ttu-id="de85c-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-401"></span></span>

<span data-ttu-id="de85c-402">Durante el proceso de inicialización, la aplicación de Office obtiene los datos del usuario actual al acceder a la propiedad **ILyncClient.Self**, que debe devolver un objeto **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="de85c-402">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="de85c-403">La interfaz **ISelf** representa al usuario de la aplicación cliente de MI conectado.</span><span class="sxs-lookup"><span data-stu-id="de85c-403">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="de85c-404">La Tabla 6 muestra los miembros que deben implementarse en la clase que hereda de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="de85c-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-405">Cualquier miembro de la interfaz **ISelf** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-405">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-406">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-406">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="de85c-407">**Tabla 6. Implementación de interfaz ISelf**</span><span class="sxs-lookup"><span data-stu-id="de85c-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="de85c-408">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-408">**Member**</span></span>|<span data-ttu-id="de85c-409">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-410">Propiedad **Contacto**</span><span class="sxs-lookup"><span data-stu-id="de85c-410">**Contact Property**</span></span>  <br/> |<span data-ttu-id="de85c-411">Obtiene el objeto **IContact** asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="de85c-412">Las propiedades de presencia, modalidades disponibles, pertenencia a grupos y tipo de contacto del usuario local se exponen a través de la propiedad **ISelf.Contact** (que devuelve un objeto **IContact**).</span><span class="sxs-lookup"><span data-stu-id="de85c-412">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="de85c-413">Durante el proceso de inicialización, la aplicación de Office tiene acceso a la propiedad **ISelf.Contact** para obtener una referencia a la información de contacto del usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-413">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="de85c-414">Usa el código siguiente para definir una clase que hereda de la interfaz **ISelf** que implementa la propiedad **Contact**.</span><span class="sxs-lookup"><span data-stu-id="de85c-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
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

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="de85c-415">Las interfaces IContactManager y _IContactManagerEvents.</span><span class="sxs-lookup"><span data-stu-id="de85c-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="de85c-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-416"></span></span>

<span data-ttu-id="de85c-417">El objeto **IContactManager** administra los contactos del usuario local, con la información de contacto propia del usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-417">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="de85c-418">La aplicación de Office utiliza un objeto **IContactManager** para acceder a los objetos **IContact** que se corresponden con los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-418">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="de85c-419">La Tabla 7 muestra los miembros que deben implementarse en la clase que hereda de **IContactManager** y **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="de85c-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-420">Cualquier miembro de la interfaz **IContactManager** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-421">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-421">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="de85c-422">Para más información sobre las interfaces **IContactManager** y **_IContactManagerEvents** y sus miembros, consulta [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) y [ UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="de85c-422">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="de85c-423">**Tabla 7. Implementación de las interfaces IContactManager y _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="de85c-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="de85c-424">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="de85c-424">**Interface**</span></span>|<span data-ttu-id="de85c-425">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-425">**Member**</span></span>|<span data-ttu-id="de85c-426">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de85c-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="de85c-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="de85c-428">Método **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="de85c-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="de85c-429">Busca o crea una nueva instancia de contacto usando el URI de contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="de85c-430">Método **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="de85c-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="de85c-431">Crea un objeto **ISubscription** que puede usarse para suscripciones por lotes o consultas.</span><span class="sxs-lookup"><span data-stu-id="de85c-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="de85c-432">Método **Lookup**</span><span class="sxs-lookup"><span data-stu-id="de85c-432">**Lookup Method**</span></span>  <br/> |<span data-ttu-id="de85c-433">Busca un contacto o grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="de85c-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="de85c-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="de85c-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="de85c-435">Evento **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="de85c-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="de85c-436">Se produce cuando se agrega un grupo a una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="de85c-436">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="de85c-437">La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="de85c-437">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="de85c-438">Evento **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="de85c-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="de85c-439">Se produce cuando se quita un grupo de una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="de85c-439">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="de85c-440">La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="de85c-440">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="de85c-441">Evento **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="de85c-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="de85c-442">Se produce cuando cambia el estado de un proveedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="de85c-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="de85c-443">Office llama a **IContactManager.GetContactByUri** para obtener información de presencia de un contacto mediante la dirección SIP del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-443">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="de85c-444">Cuando un contacto está configurado para una dirección SIP en Active Directory, Office determina esta dirección para un contacto y llama a **GetContactByUri**, al pasar la dirección SIP del contacto para el parámetro __contactUri_.</span><span class="sxs-lookup"><span data-stu-id="de85c-444">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="de85c-445">Cuando Office no puede determinar la dirección SIP para un contacto, llama al método **IContactManager.Lookup** para encontrar el SIP mediante el servicio de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-445">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="de85c-446">Aquí Office pasa los mejores datos que puede encontrar para el contacto (por ejemplo, solo la dirección de correo del contacto).</span><span class="sxs-lookup"><span data-stu-id="de85c-446">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="de85c-447">El método **Lookup** devuelve de forma asincrónica un objeto **AsynchronousOperation**.</span><span class="sxs-lookup"><span data-stu-id="de85c-447">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="de85c-448">Cuando invoca la retrollamada, el método **Lookup** debe devolver el éxito o fracaso de la operación además del URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-448">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
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

<span data-ttu-id="de85c-449">La aplicación de Office debe suscribirse a los cambios de presencia de un contacto individual.</span><span class="sxs-lookup"><span data-stu-id="de85c-449">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="de85c-450">Por lo tanto, cuando cambia el estado de presencia de un contacto, el servidor de MI le avisa a la aplicación cliente de MI, lo que alerta a la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="de85c-450">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="de85c-451">Para ello, la aplicación de Office llama al método **IContactManager.CreateSubscription** para crear un nuevo objeto **IContactSubscription** para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="de85c-451">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
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

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="de85c-452">Interfaces IGroup e IGroupCollection.</span><span class="sxs-lookup"><span data-stu-id="de85c-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="de85c-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-453"></span></span>

<span data-ttu-id="de85c-454">El objeto **IGroup** representa una colección de contactos con propiedades adicionales para identificar la colección de contactos mediante un nombre de grupo colectivo.</span><span class="sxs-lookup"><span data-stu-id="de85c-454">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="de85c-455">Un objeto **IGroupCollection** representa una colección de objetos **IGroup** definidos por el usuario local y la aplicación de cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-455">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="de85c-456">La aplicación de Office usa los objetos **IGroupCollection** y **IGroup** para tener acceso a los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="de85c-456">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="de85c-457">La Tabla 9 muestra los miembros que deben implementarse en las clases que heredan de **IGroup** e **IGroupCollection** en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="de85c-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="de85c-458">Cualquier miembro de la interfaz **IGroup** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-459">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="de85c-460">Para más información sobre las interfaces **IGroup** e **IGroupCollection** y sus miembros, consulta [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) y [ UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="de85c-460">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="de85c-461">**Tabla 9. Implementación de las interfaces IGroup e IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="de85c-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="de85c-462">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="de85c-462">**Interface**</span></span>|<span data-ttu-id="de85c-463">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-463">**Member**</span></span>|<span data-ttu-id="de85c-464">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de85c-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="de85c-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="de85c-466">Propiedad **Count**</span><span class="sxs-lookup"><span data-stu-id="de85c-466">**Count** property</span></span>  <br/> |<span data-ttu-id="de85c-467">Devuelve el número de objeto **IGroup** de la colección</span><span class="sxs-lookup"><span data-stu-id="de85c-467">Returns a **Long** indicating the count of objects in the specified collection.</span></span>  <br/> |
||<span data-ttu-id="de85c-468">Propiedad **Item**</span><span class="sxs-lookup"><span data-stu-id="de85c-468">**Item** property</span></span>  <br/> |<span data-ttu-id="de85c-469">Devuelve el objeto **IGroup** en el índice especificado en la colección.</span><span class="sxs-lookup"><span data-stu-id="de85c-469">Returns the **MailMergeDataSource** object at the specified index position in the MailMergeDataSources collection.</span></span>  <br/> |
|<span data-ttu-id="de85c-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="de85c-470">**IGroup**</span></span> <br/> |<span data-ttu-id="de85c-471">Propiedad **Id**</span><span class="sxs-lookup"><span data-stu-id="de85c-471">**ID Property**</span></span>  <br/> |<span data-ttu-id="de85c-472">Devuelve el id. del grupo.</span><span class="sxs-lookup"><span data-stu-id="de85c-472">Gets the ID of the section group.</span></span>  <br/> |
   
<span data-ttu-id="de85c-473">Cuando la aplicación de Office obtiene la información de usuario local, tiene acceso a la pertenencia del contacto (usuario local) al llamar a la propiedad **IContact.CustomGroups** que devuelve un objeto **IGroupCollection**.</span><span class="sxs-lookup"><span data-stu-id="de85c-473">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="de85c-474">**IGroupCollection** debe contener una matriz (o **lista**) de objetos **IGroup**.</span><span class="sxs-lookup"><span data-stu-id="de85c-474">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="de85c-475">La clase que se deriva de **IGroupCollection** debe exponer una propiedad **Count**, que devuelve el número de elementos de la colección y un método indizador, **this(int)**, que devuelve un objeto **IGroup** de la colección.</span><span class="sxs-lookup"><span data-stu-id="de85c-475">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="de85c-476">Interfaz IContactSubscription.</span><span class="sxs-lookup"><span data-stu-id="de85c-476">IContactSubscription interface</span></span>
<span data-ttu-id="de85c-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-477"></span></span>

<span data-ttu-id="de85c-478">La interfaz **IContactSubscription** te permite especificar los contactos para recibir actualizaciones de la información de presencia y los tipos de información de presencia que activan una notificación.</span><span class="sxs-lookup"><span data-stu-id="de85c-478">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="de85c-479">Las aplicaciones de Office utilizan un objeto **IContactSubscription** para registrar cambios al estado de presencia del contacto</span><span class="sxs-lookup"><span data-stu-id="de85c-479">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="de85c-480">La Tabla 10 muestra los miembros que deben implementarse en las clases que heredan de **IContactSuscription**.</span><span class="sxs-lookup"><span data-stu-id="de85c-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-481">Cualquier miembro de la interfaz **IContactSubscription** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-482">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="de85c-483">Para más información sobre la interfaz **IContactSubscription** y sus miembros, consulta [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="de85c-483">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="de85c-484">**Tabla 10. Implementación de interfaz IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="de85c-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="de85c-485">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-485">**Member**</span></span>|<span data-ttu-id="de85c-486">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-487">Método **AddContact**</span><span class="sxs-lookup"><span data-stu-id="de85c-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="de85c-488">Agrega un contacto al objeto de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="de85c-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="de85c-489">Método **Subscribe**</span><span class="sxs-lookup"><span data-stu-id="de85c-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="de85c-490">Ayuda de la aplicación cliente de MI a supervisar la presencia de un contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="de85c-491">La interfaz **IContactSubscription** debe contener una referencia a todos los objetos **IContact** que supervisa, mediante el uso de una matriz o una **Lista**.</span><span class="sxs-lookup"><span data-stu-id="de85c-491">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="de85c-492">El método **IContactSubscription.AddContact** agrega un objeto **IContact** a la estructura de datos subyacente del objeto **IContactSubscription**, lo que agrega un contacto nuevo para supervisar los cambios de presencia.</span><span class="sxs-lookup"><span data-stu-id="de85c-492">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="de85c-493">El método **IContactSubscription.Subscribe** permite que una aplicación cliente de MI acceda a observadores de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-493">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="de85c-494">Puede usar una estrategia de sondeo para obtener la presencia del servidor de los contactos para los que se haya suscrito la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="de85c-494">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="de85c-495">El método **Subscribe** es útil en situaciones donde se solicita la presencia de alguien de fuera de la lista de contactos de un usuario (por ejemplo, de una red pública de mayor tamaño).</span><span class="sxs-lookup"><span data-stu-id="de85c-495">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="de85c-496">Interfaz IContactEndPoint.</span><span class="sxs-lookup"><span data-stu-id="de85c-496">IContactEndPoint interface</span></span>
<span data-ttu-id="de85c-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-497"></span></span>

<span data-ttu-id="de85c-498">**IContactEndPoint** representa un número de teléfono de la colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="de85c-499">La Tabla 11 muestra los miembros que deben implementarse en las clases que heredan de **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="de85c-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-500">Cualquier miembro de la interfaz **IContactEndPoint**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-501">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="de85c-502">Para más información sobre la interfaz **IContactEndPoint** y sus miembros, consulta [UCCollaborationLib.IContactEndPoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="de85c-502">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="de85c-503">**Tabla 11. Implementación de la interfaz IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="de85c-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="de85c-504">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-504">**Member**</span></span>|<span data-ttu-id="de85c-505">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-506">Propiedad **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="de85c-506">**DisplayName Property**</span></span>  <br/> |<span data-ttu-id="de85c-507">Obtiene la cadena para mostrar</span><span class="sxs-lookup"><span data-stu-id="de85c-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="de85c-508">Propiedad **Type**</span><span class="sxs-lookup"><span data-stu-id="de85c-508">**Type** property</span></span>  <br/> |<span data-ttu-id="de85c-509">Obtiene el tipo de punto de contacto</span><span class="sxs-lookup"><span data-stu-id="de85c-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="de85c-510">Propiedad **Uri**</span><span class="sxs-lookup"><span data-stu-id="de85c-510">**Uri Property**</span></span>  <br/> |<span data-ttu-id="de85c-511">Obtiene el URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="de85c-512">Interfaz ILocaleString</span><span class="sxs-lookup"><span data-stu-id="de85c-512">ILocaleString interface</span></span>
<span data-ttu-id="de85c-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="de85c-513"></span></span>

<span data-ttu-id="de85c-514">**ILocaleString** es una estructura de cadena localizada que contiene una cadena localizada y el ID de la localización de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="de85c-514">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="de85c-515">La interfaz **ILocaleString** se utiliza para dar formato a la cadena de estado personalizado en la tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="de85c-515">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="de85c-516">La Tabla 12 muestra los miembros que deben implementarse en las clases que heredan de **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="de85c-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de85c-517">Cualquier miembro de la interfaz **ILocaleString** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="de85c-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="de85c-518">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="de85c-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="de85c-519">Para más información sobre la interfaz **ILocaleString** y sus miembros, consulta [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="de85c-519">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="de85c-520">**Tabla 12. Implementación de interfaz ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="de85c-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="de85c-521">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="de85c-521">**Member**</span></span>|<span data-ttu-id="de85c-522">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de85c-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de85c-523">Propiedad **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="de85c-523">**LocaleID Property**</span></span>  <br/> |<span data-ttu-id="de85c-524">Obtiene la id. de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="de85c-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="de85c-525">Propiedad **Value**</span><span class="sxs-lookup"><span data-stu-id="de85c-525">Value property</span></span>  <br/> |<span data-ttu-id="de85c-526">Obtiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="de85c-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de85c-527">Ver también</span><span class="sxs-lookup"><span data-stu-id="de85c-527">See also</span></span>

- <span data-ttu-id="de85c-528">Espacio de nombre [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="de85c-528">[UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

