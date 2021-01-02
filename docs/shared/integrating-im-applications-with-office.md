---
title: Integración de aplicaciones de mensajería instantánea con Office
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013 y siguientes, como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.
localization_priority: Priority
ms.openlocfilehash: 3494d42af82c174469272928286c3fc5f847eebc
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734234"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="670a6-103">Integración de aplicaciones de mensajería instantánea con Office</span><span class="sxs-lookup"><span data-stu-id="670a6-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="670a6-104">Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013, Office 2016, Office 2019, y Office 365 como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="670a6-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, Office 2016, Office 2019, and Office 365, including displaying presence and sending instant messages from the contact card.</span></span>
  
## <a name="introduction"></a><span data-ttu-id="670a6-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="670a6-105">Introduction</span></span>
<span data-ttu-id="670a6-106"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-106"><a name="off15_IMIntegration_Intro"> </a></span></span>

<span data-ttu-id="670a6-107">Office 2013 (y siguientes) ofrece una completa integración con aplicaciones cliente de MI, incluidos Lync 2013 y Teams.</span><span class="sxs-lookup"><span data-stu-id="670a6-107">Office 2013 (and later versions) provides rich integration with IM client applications, including Lync 2013 and Teams.</span></span> <span data-ttu-id="670a6-108">Esta integración proporciona a los usuarios capacidades de MI desde dentro de Word, Excel, PowerPoint, Outlook, Visio, Project y OneNote, así como la integración de presencia en las páginas de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="670a6-108">This integration provides users with IM capabilities from within Word, Excel, PowerPoint, Outlook, Visio, Project, and OneNote as well as providing presence integration on SharePoint pages.</span></span> <span data-ttu-id="670a6-109">Los usuarios pueden ver la foto, el nombre, el estado de presencia y los datos de contacto de los usuarios de su lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="670a6-109">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="670a6-110">Pueden iniciar una sesión de MI, realizar una videollamada o una llamada telefónica directamente desde la tarjeta de contactos (el elemento de la IU en Office que expone opciones de información de contacto y comunicación).</span><span class="sxs-lookup"><span data-stu-id="670a6-110">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office that surfaces contact information and communication options).</span></span> <span data-ttu-id="670a6-111">Office te permite mantenerte conectado a tus contactos sin tener que salir de tus correos o documentos.</span><span class="sxs-lookup"><span data-stu-id="670a6-111">Office makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="670a6-112">Este artículo usa el término aplicación cliente de MI para hacer referencia específicamente para la aplicación instalada en el equipo de un usuario que se comunica con el servicio de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-112">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="670a6-113">Por ejemplo, Lync 2013 y Teams se consideran aplicaciones cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-113">For example, Lync 2013 and Teams are considered an IM client applications.</span></span> <span data-ttu-id="670a6-114">Este artículo no proporciona detalles acerca de cómo se comunica la aplicación cliente de MI con el servicio de MI o acerca del servicio de MI en sí mismo.</span><span class="sxs-lookup"><span data-stu-id="670a6-114">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="670a6-115">Puedes personalizar una aplicación cliente de MI para que se comunique con Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-115">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="670a6-116">En concreto, puedes modificar la aplicación de MI para que muestre la siguiente información dentro de la IU de Office:</span><span class="sxs-lookup"><span data-stu-id="670a6-116">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="670a6-117">Foto del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-117">Contact photo.</span></span>
    
- <span data-ttu-id="670a6-118">Nombre de contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-118">Contact name.</span></span>
    
- <span data-ttu-id="670a6-119">Nota de estado personal del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-119">Contact personal status note.</span></span>
    
- <span data-ttu-id="670a6-120">Estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-120">Contact presence status.</span></span>
    
- <span data-ttu-id="670a6-121">Cadena de disponibilidad del contacto (por ejemplo, "Disponible" o "Fuera de la oficina").</span><span class="sxs-lookup"><span data-stu-id="670a6-121">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="670a6-122">Cadena de función del contacto (por ejemplo, "listo para video").</span><span class="sxs-lookup"><span data-stu-id="670a6-122">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="670a6-123">Inicio de MI con un solo clic.</span><span class="sxs-lookup"><span data-stu-id="670a6-123">One-click IM launch.</span></span>
    
- <span data-ttu-id="670a6-124">Inicio de videollamada con un solo clic.</span><span class="sxs-lookup"><span data-stu-id="670a6-124">One-click video call launch.</span></span>
    
- <span data-ttu-id="670a6-125">Inicio de llamada de teléfono con un solo clic (incluye SIP, número de teléfono, correo de voz y llamada a un número nuevo).</span><span class="sxs-lookup"><span data-stu-id="670a6-125">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="670a6-126">Administración de contactos (agregar al grupo de MI).</span><span class="sxs-lookup"><span data-stu-id="670a6-126">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="670a6-127">Ubicación y zona horaria del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-127">Contact location and time zone.</span></span>
    
- <span data-ttu-id="670a6-128">Datos, número de teléfono, dirección de correo, puesto y nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-128">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="670a6-129">**Ilustración 1. Tarjeta de contactos en Office 2013**</span><span class="sxs-lookup"><span data-stu-id="670a6-129">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="670a6-130">![Tarjeta de personas en Office 2013](media/ocom15_peoplecard.png "Tarjeta de personas en Office 2013")</span><span class="sxs-lookup"><span data-stu-id="670a6-130">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="670a6-131">Para habilitar la integración con Office, una aplicación cliente de MI debe implementar un conjunto de interfaces de conexión que proporciona Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-131">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="670a6-132">Se incluyen las API para esta integración en el espacio de nombre [UCCollborationLib](https://docs.microsoft.com/previous-versions/office/communications/ff398475(v=ocs.14)) contenido en el archivo Microsoft.Office.UC.dll, que se instala con las versiones de Office 2013 que incluyen Lync o Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="670a6-132">The APIs for this integration are included in the [UCCollborationLib](https://docs.microsoft.com/previous-versions/office/communications/ff398475(v=ocs.14)) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="670a6-133">El espacio de nombre **UCCollaborationLib** incluye las interfaces que debes implementar para la integración con Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-133">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="670a6-134">La biblioteca de tipos para las interfaces necesarias está incrustada en Lync 2013 o Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="670a6-134">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="670a6-135">Para integradores de terceros, esto solo funciona cuando los equipos de destino tienen instalado Lync 2013 y en Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="670a6-135">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="670a6-136">Si realizas la integración con Office Standard, deberás extraer la biblioteca de tipos e instalarla en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="670a6-136">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="670a6-137">El [SDK de Lync 2013](https://www.microsoft.com/download/details.aspx?id=36824) incluye el archivo Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="670a6-137">The [Lync 2013 SDK](https://www.microsoft.com/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="670a6-138">Algunas aplicaciones de Office 2010 puede integrarse de forma similar con una aplicación de proveedores de MI de terceros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 y SharePoint Server 2010 (con un control ActiveX).</span><span class="sxs-lookup"><span data-stu-id="670a6-138">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="670a6-139">Muchos de los pasos necesarios para la integración con Office 2013 se aplican también a Office 2010.</span><span class="sxs-lookup"><span data-stu-id="670a6-139">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="670a6-140">Hay varias diferencias clave en la forma en la que Office 2010 se integra con una aplicación de proveedor de MI:</span><span class="sxs-lookup"><span data-stu-id="670a6-140">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="670a6-141">Office 2010 no muestra la foto del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-141">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="670a6-142">Debes descargar el archivo Microsoft.Office.Uc.dll por separado de Office 2010.</span><span class="sxs-lookup"><span data-stu-id="670a6-142">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="670a6-143">El [SDK de Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) incluye el archivo Microsoft.Office.UC.dll para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="670a6-143">The [Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="670a6-144">Cuando la aplicación de Office llama al método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) en la aplicación cliente de MI, pasa la cadena "14.0.0.0".</span><span class="sxs-lookup"><span data-stu-id="670a6-144">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="670a6-145">Office 2010 enumera todos los grupos y contactos en cuanto se conecta a una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-145">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="670a6-146">Integración de Office con una aplicación cliente de MI</span><span class="sxs-lookup"><span data-stu-id="670a6-146">How Office integrates with an IM client application</span></span>
<span data-ttu-id="670a6-147"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-147"><a name="off15_IMIntegration_How"> </a></span></span>

<span data-ttu-id="670a6-148">Cuando se inicia una aplicación de Office 2013 (y siguientes), atraviesa el siguiente proceso para integrarse con la aplicación cliente de MI predeterminada:</span><span class="sxs-lookup"><span data-stu-id="670a6-148">When an Office 2013 (or higher) application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="670a6-149">Comprueba el registro para descubrir la aplicación cliente de MI predeterminada y, a continuación, se conecta a ella.</span><span class="sxs-lookup"><span data-stu-id="670a6-149">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="670a6-150">Se autentica con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-150">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="670a6-151">Se conecta a interfaces específicas expuestas por la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-151">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="670a6-152">Determina las funciones del usuario que inició sesión actualmente (usuario local), incluida la obtención de los contactos del usuario, la determinación de la presencia del usuario y la determinación de las capacidades de MI del usuario (mensajería instantánea, chat de video, VOIP, etc.).</span><span class="sxs-lookup"><span data-stu-id="670a6-152">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="670a6-153">Obtiene la información de presencia de los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-153">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="670a6-154">Cuando se cierra la aplicación cliente de MI, la aplicación de Office se desconecta de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="670a6-154">When the IM client application shuts down, the Office application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="670a6-155">Descubrir la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="670a6-155">Discovering the IM application</span></span>

<span data-ttu-id="670a6-156">La aplicación de Office busca varias teclas y entradas específicas en el registro para obtener información sobre la aplicación cliente de MI de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="670a6-156">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="670a6-157">Si detecta una aplicación cliente de MI de forma predeterminada, a continuación, intenta conectarse a ella.</span><span class="sxs-lookup"><span data-stu-id="670a6-157">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="670a6-158">El proceso que realiza la aplicación de Office para obtener información sobre la aplicación cliente de MI predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="670a6-158">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="670a6-159">La aplicación de Office intenta ver si se establece la subclave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp en el registro y lee el nombre de aplicación que aparece allí.</span><span class="sxs-lookup"><span data-stu-id="670a6-159">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="670a6-160">La aplicación de Office, a continuación, lee la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning y controla el valor para detectar cambios.</span><span class="sxs-lookup"><span data-stu-id="670a6-160">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="670a6-161">La aplicación de Office a continuación lee la clave del registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ y obtiene los valores de ProcessName e identificador de clase (CLSID) almacenados allí.</span><span class="sxs-lookup"><span data-stu-id="670a6-161">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="670a6-162">Una vez que la aplicación cliente de MI completó correctamente su secuencia de inicio y registró todas las clases correctamente para la integración de presencia, establece la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning en "2", lo que indica que se está ejecutando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="670a6-162">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="670a6-163">Cuando la aplicación de Office detecta que la clave de HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning se estableció en "2", comprueba la lista de procesos en ejecución en el equipo para ver el nombre de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-163">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="670a6-164">Una vez que la aplicación de Office encuentra el proceso que utiliza la aplicación cliente de MI, la aplicación de Office llama a **CoCreateInstance** mediante CLSID para establecer una conexión con la aplicación cliente de MI como servidor COM fuera del proceso.</span><span class="sxs-lookup"><span data-stu-id="670a6-164">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="670a6-165">Autenticación de la conexión a la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="670a6-165">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="670a6-166">Después de que la aplicación de Office establece una conexión con la aplicación cliente de MI, a continuación, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="670a6-166">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="670a6-167">La aplicación de Office llama al método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para comprobar la interfaz [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="670a6-167">The Office application calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="670a6-168">La aplicación de Office, a continuación, llama al método **IUCOfficeIntegration.GetAuthenticationInfo**, pasando la versión más alta de integración compatible (por ejemplo, "15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="670a6-168">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="670a6-169">Si la aplicación cliente de MI es compatible con la versión de Office que se pasa como un parámetro, la aplicación devuelve la siguiente cadena XML codificada de forma rígida al código de llamada:</span><span class="sxs-lookup"><span data-stu-id="670a6-169">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="670a6-170">Por motivos heredados, la aplicación cliente de MI debe devolver el valor exacto `<authenticationinfo>` a la llamada a **GetAuthenticationInfo** si se admite la versión de Office pasado como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="670a6-170">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="670a6-171">Si la aplicación cliente no puede devolver un valor, la aplicación de Office llama al método **GetAuthenticationInfo** nuevamente con la siguiente versión más alta compatible de Office (por ejemplo, "14.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="670a6-171">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="670a6-172">Cuando Office determina que la aplicación cliente de MI es compatible con la integración de presencia y MI, se conecta a un conjunto requerido de interfaces para finalizar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="670a6-172">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="670a6-173">(Para obtener más información, consulta [Conectarse a interfaces necesarias](#off15_IMIntegration_HowConnect).)</span><span class="sxs-lookup"><span data-stu-id="670a6-173">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="670a6-174">Si la aplicación de Office, produce un error en cualquiera de los pasos anteriores, retrocede y no se establece la integración de presencia durante la sesión de la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-174">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="670a6-175">Conexión a las interfaces necesarias</span><span class="sxs-lookup"><span data-stu-id="670a6-175">Connecting to required interfaces</span></span>
<span data-ttu-id="670a6-176"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-176"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="670a6-177">Después de autenticar la conexión a la aplicación cliente de MI, la aplicación de Office intenta conectarse a un conjunto de interfaces necesarias que debe exponer la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-177">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="670a6-178">La aplicación de Office lo logra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="670a6-178">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="670a6-179">La aplicación de Office obtiene un objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceLyncClient** desde la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="670a6-179">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="670a6-180">La aplicación de Office obtiene un objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceAutomation** desde la enumeración **OIInterface**.</span><span class="sxs-lookup"><span data-stu-id="670a6-180">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="670a6-181">La aplicación de Office configura la escucha de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient).</span><span class="sxs-lookup"><span data-stu-id="670a6-181">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="670a6-182">La aplicación de Office, configura la escucha de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="670a6-182">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="670a6-183">La aplicación de Office obtiene el estado de inicio de sesión de la aplicación cliente de MI mediante el acceso a la propiedad **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="670a6-183">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="670a6-184">La aplicación de Office obtiene las capacidades de la aplicación cliente de MI al llamar al método **IUCOfficeIntegration.GetSupportedFeatures**, que devuelve una marca de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="670a6-184">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="670a6-185">La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Self** para obtener una referencia a un objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="670a6-185">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="670a6-186">Recuperar las capacidades del usuario local</span><span class="sxs-lookup"><span data-stu-id="670a6-186">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="670a6-187"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-187"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="670a6-188">La aplicación de Office obtiene las capacidades del usuario local mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="670a6-188">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="670a6-189">Si la aplicación cliente de MI es compatible con la interfaz **IClient2**, Office intenta obtener un objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) mediante el acceso a la propiedad **IClient2.PrivateContactManager**.</span><span class="sxs-lookup"><span data-stu-id="670a6-189">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="670a6-190">Si la aplicación de MI no es compatible con la interfaz **IClient2**, la aplicación de Office intenta obtener un objeto **IContactManager** mediante el acceso a la propiedad **ILyncClient.ContactManager**.</span><span class="sxs-lookup"><span data-stu-id="670a6-190">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="670a6-191">La aplicación cliente de MI debe devolver correctamente un objeto **IContactManager** antes de que se puedan establecer otras capacidades de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-191">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="670a6-192">La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Uri** y después llama a **IContactManager.GetContactByUri** para obtener el objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-192">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="670a6-193">A continuación, la aplicación de Office hace varias llamadas a **IContact.CanStart** para establecer las capacidades del usuario local, al pasar los valores de **ModalityTypes.ucModalityInstantMessage** y **ModalityTypes.ucModalityAudioVideo** sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="670a6-193">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="670a6-194">Recuperar presencia de contactos</span><span class="sxs-lookup"><span data-stu-id="670a6-194">Retrieving contact presence</span></span>
<span data-ttu-id="670a6-195"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-195"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="670a6-196">La aplicación de Office obtiene la presencia de contactos, incluido el usuario local, mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="670a6-196">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="670a6-197">La aplicación de Office llama a **IContact.GetContactInformation** para obtener un elemento de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-197">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="670a6-198">A continuación, la aplicación de Office se suscribe a los cambios de estado de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-198">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="670a6-199">Llama a **IContactManager.CreateSubscription** para obtener un objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="670a6-199">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="670a6-200">A continuación, llama a **IContactSubscription.AddContact** para agregar el contacto a la suscripción y luego llama a **IContactSubscription.Subscribe** para obtener los cambios de estado del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-200">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="670a6-201">Si la aplicación de MI es compatible con **IContact2**, Office intenta obtener información de presencia llamando a **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="670a6-201">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="670a6-202">A continuación, la aplicación de Office recupera las propiedades de la presencia del contacto llamando a **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="670a6-202">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="670a6-203">La aplicación de Office puede obtener un segundo conjunto de propiedades de presencia si obtiene acceso a la propiedad **IContact.Settings**.</span><span class="sxs-lookup"><span data-stu-id="670a6-203">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="670a6-204">Por último, la aplicación de Office obtiene la pertenencia del grupo del contacto al acceder a la propiedad **IContact.CustomGroups**.</span><span class="sxs-lookup"><span data-stu-id="670a6-204">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="670a6-205">Esto le devuelve una colección [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que incluye a todos los objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) a los que pertenece el contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-205">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="670a6-206">Desconexión de la aplicación de MI</span><span class="sxs-lookup"><span data-stu-id="670a6-206">Disconnecting from the IM application</span></span>
<span data-ttu-id="670a6-207"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-207"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="670a6-208">Cuando la aplicación de Office detecta el evento **OnShuttingDown** desde la aplicación de MI, se desconecta silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="670a6-208">When the Office application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="670a6-209">Sin embargo, si cierra la aplicación de Office antes de la aplicación de MI, la aplicación de Office no garantiza que la conexión se limpie.</span><span class="sxs-lookup"><span data-stu-id="670a6-209">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="670a6-210">La aplicación de MI debe controlar pérdidas de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="670a6-210">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="670a6-211">Entradas y claves del registro de configuración</span><span class="sxs-lookup"><span data-stu-id="670a6-211">Setting registry keys and entries</span></span>
<span data-ttu-id="670a6-212"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-212"><a name="off15_IMIntegration_SetRegistry"> </a></span></span>

<span data-ttu-id="670a6-213">Como se indicó anteriormente, las aplicaciones de Office compatibles con MI buscan teclas, entradas y valores específicos en el registro para obtener información sobre la aplicación cliente de MI a la cual conectarse.</span><span class="sxs-lookup"><span data-stu-id="670a6-213">As mentioned previously, the IM-capable Office applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="670a6-214">Estos valores de registro le proporcionan a la aplicación de Office el nombre del proceso y CLSID de la clase que actúa como punto de entrada al modelo de objeto de la aplicación cliente de MI (es decir, la clase que implementa la interfaz **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="670a6-214">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="670a6-215">La aplicación de Office crea conjuntamente la clase y se conecta como cliente al servidor COM fuera de proceso en la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-215">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="670a6-216">Usa la tabla 1 para identificar las claves, entradas y valores que deben escribirse en el registro para integrar una aplicación cliente de MI con Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-216">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="670a6-217">**Tabla 1. Claves del registro para configurar la aplicación cliente de MI predeterminada**</span><span class="sxs-lookup"><span data-stu-id="670a6-217">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="670a6-218">**Clave**</span><span class="sxs-lookup"><span data-stu-id="670a6-218">**Key**</span></span>|<span data-ttu-id="670a6-219">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="670a6-219">**Entry**</span></span>|<span data-ttu-id="670a6-220">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="670a6-220">**Type**</span></span>|<span data-ttu-id="670a6-221">**Valor**</span><span class="sxs-lookup"><span data-stu-id="670a6-221">**Value**</span></span>|<span data-ttu-id="670a6-222">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="670a6-222">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="670a6-223">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span><span class="sxs-lookup"><span data-stu-id="670a6-223">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="670a6-224">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="670a6-224">FriendlyName</span></span>  <br/> |<span data-ttu-id="670a6-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="670a6-225">REG_SZ</span></span>  <br/> |<span data-ttu-id="670a6-226">El nombre de la aplicación cliente de MI de terceros.</span><span class="sxs-lookup"><span data-stu-id="670a6-226">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="670a6-227">MI de Litware 2012</span><span class="sxs-lookup"><span data-stu-id="670a6-227">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="670a6-228">ProcessName</span><span class="sxs-lookup"><span data-stu-id="670a6-228">ProcessName</span></span>  <br/> |<span data-ttu-id="670a6-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="670a6-229">REG_SZ</span></span>  <br/> |<span data-ttu-id="670a6-230">El nombre del proceso de la aplicación cliente de MI de terceros.</span><span class="sxs-lookup"><span data-stu-id="670a6-230">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="670a6-231">litware.exe</span><span class="sxs-lookup"><span data-stu-id="670a6-231">litware.exe</span></span>  <br/> |
||<span data-ttu-id="670a6-232">GUID</span><span class="sxs-lookup"><span data-stu-id="670a6-232">GUID</span></span>  <br/> |<span data-ttu-id="670a6-233">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="670a6-233">REG_SZ</span></span>  <br/> |<span data-ttu-id="670a6-234">Un identificador de clase (CLSID) para la clase de creación conjunta de raíz en la aplicación de MI (la clase que implementa la interfaz **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="670a6-234">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="670a6-235">(Un GUID)</span><span class="sxs-lookup"><span data-stu-id="670a6-235">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="670a6-236">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="670a6-236">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="670a6-237">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="670a6-237">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="670a6-238">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="670a6-238">REG_SZ</span></span>  <br/> |<span data-ttu-id="670a6-239">El nombre de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-239">The name of the IM client application.</span></span> <span data-ttu-id="670a6-240">Debe ser el mismo que el nombre de la clave del registro de nivel superior (subárbol) en HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="670a6-240">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="670a6-241">Litware</span><span class="sxs-lookup"><span data-stu-id="670a6-241">Litware</span></span>  <br/> |
|<span data-ttu-id="670a6-242">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span><span class="sxs-lookup"><span data-stu-id="670a6-242">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="670a6-243">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="670a6-243">UpAndRunning</span></span>  <br/> |<span data-ttu-id="670a6-244">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="670a6-244">REG_DWORD</span></span>  <br/> | <span data-ttu-id="670a6-245">Valor entero entre 0 y 2:</span><span class="sxs-lookup"><span data-stu-id="670a6-245">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="670a6-246">0—No en ejecución</span><span class="sxs-lookup"><span data-stu-id="670a6-246">0—Not running</span></span>  <br/>  <span data-ttu-id="670a6-247">1—Iniciándose</span><span class="sxs-lookup"><span data-stu-id="670a6-247">1—Starting</span></span>  <br/>  <span data-ttu-id="670a6-248">2—En ejecución</span><span class="sxs-lookup"><span data-stu-id="670a6-248">2—Running</span></span>  <br/> <br/><span data-ttu-id="670a6-249">**NOTA**: la clave del registro de nombre de aplicación debe ser igual al valor de la entrada DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="670a6-249">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="670a6-250">Implementar las interfaces necesarias para la integración con Office</span><span class="sxs-lookup"><span data-stu-id="670a6-250">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="670a6-251"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-251"><a name="off15_IMIntegration_ImplementRequired"> </a></span></span>

<span data-ttu-id="670a6-252">Hay tres interfaces del espacio de nombre **UCCollaborationLib** que debe implementar el archivo ejecutable (o servidor COM) de una aplicación cliente de MI para que se pueda integrar con Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-252">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="670a6-253">Si no se implementan estas interfaces, la aplicación de Office retrocede durante el proceso de inicialización y no se establece la conexión con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-253">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="670a6-254">Las interfaces necesarias son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="670a6-254">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="670a6-255">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). Si bien no es necesaria, la interfaz **_IUCOfficeIntegrationEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="670a6-255">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="670a6-256">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). Si bien no es necesaria, la interfaz **_ILyncClientEvents** también debe implementarse en la misma clase derivada.</span><span class="sxs-lookup"><span data-stu-id="670a6-256">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="670a6-257">IAutomation</span><span class="sxs-lookup"><span data-stu-id="670a6-257">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="670a6-258">Interfaz IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="670a6-258">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="670a6-259"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-259"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span></span>

<span data-ttu-id="670a6-260">La interfaz **IUCOfficeIntegration** proporciona el punto de entrada para que una aplicación de Office se conecte a la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-260">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="670a6-261">La interfaz define tres métodos que una aplicación de Office llama como parte del proceso de iniciar una conexión con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-261">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="670a6-262">La clase que implementa la interfaz **IUCOfficeIntegration** se debe poder cocrear para que Office pueda cocrear una instancia de ella.</span><span class="sxs-lookup"><span data-stu-id="670a6-262">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="670a6-263">Además, debe exponer la CLSID que se introduce como el valor de la entrada de GUID en la clave de registro HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_</span><span class="sxs-lookup"><span data-stu-id="670a6-263">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="670a6-264">La clase que hereda de **IUCOfficeIntegration** también debe implementar la interfaz **_IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="670a6-264">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="670a6-265">La interfaz **_IUCOfficeIntegrationEvents** contiene los miembros que exponen los controladores de eventos de la interfaz **IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="670a6-265">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="670a6-266">La Tabla 2 muestra los miembros que deben implementarse en la clase que hereda de **IUCOfficeIntegration** y **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="670a6-266">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-267">Para más información sobre las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegrationEvents** y sus miembros, consulta [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) y [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="670a6-267">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="670a6-268">**Tabla 2. Implementación de las interfaces IUCOfficeIntegration y _IUCOfficeIntegrationEvents interfaces**</span><span class="sxs-lookup"><span data-stu-id="670a6-268">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="670a6-269">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="670a6-269">**Interface**</span></span>|<span data-ttu-id="670a6-270">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-270">**Member**</span></span>|<span data-ttu-id="670a6-271">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-271">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="670a6-272">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="670a6-272">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="670a6-273">Método **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="670a6-273">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="670a6-274">Obtiene la cadena de información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="670a6-274">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="670a6-275">Método **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="670a6-275">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="670a6-276">Obtiene la interfaz de una versión específica.</span><span class="sxs-lookup"><span data-stu-id="670a6-276">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="670a6-277">Método **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="670a6-277">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="670a6-278">Obtiene las características de integración de Office compatibles.</span><span class="sxs-lookup"><span data-stu-id="670a6-278">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="670a6-279">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="670a6-279">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="670a6-280">Evento **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="670a6-280">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="670a6-281">El evento que se produce cuando la aplicación cliente de MI está intentando cerrarse.</span><span class="sxs-lookup"><span data-stu-id="670a6-281">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="670a6-282">Usa el código siguiente para definir una clase que herede de las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegration** dentro de una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-282">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
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

<span data-ttu-id="670a6-283">El método **GetAuthenticationInfo** toma una cadena como argumento para el parámetro _version_.</span><span class="sxs-lookup"><span data-stu-id="670a6-283">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="670a6-284">Cuando la aplicación de Office llama a este método, pasa una de las dos cadenas del argumento, según la versión de Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-284">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="670a6-285">Cuando la aplicación de Office proporciona el método con la versión de Office compatible con la aplicación cliente de MI (es decir, compatible con la funcionalidad), el método **GetAuthenticationInfo** devuelve una cadena XML codificada de forma rígida `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="670a6-285">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="670a6-286">Usa el código siguiente para implementar un método **GetAuthentication** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-286">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="670a6-287">El método **GetInterface** envía las referencias a clases al código de llamada, dependiendo de lo que se pasa como argumento para el parámetro de la _interface_.</span><span class="sxs-lookup"><span data-stu-id="670a6-287">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="670a6-288">Cuando una aplicación de Office llama al método **GetInterface**, pasa uno de los dos valores para el parámetro de la interfaz: la constante **oiInterfaceILyncClient** (1) o **la constante oiInterfaceIAutomation** (2) de la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="670a6-288">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="670a6-289">Si la aplicación de Office pasa la constante **oiInterfaceILyncClient**, el método **GetInterface** devuelve una referencia a una clase que implementa la interfaz **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="670a6-289">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="670a6-290">Si la aplicación de Office pasa la constante **oiInterfaceIAutomation**, el método **GetInterface** devuelve una clase que implementa la interfaz **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="670a6-290">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="670a6-291">Usa el siguiente código de ejemplo para implementar el método **GetInterface** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-291">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="670a6-292">El método **GetSupportedFeatures** devuelve información sobre las características de MI compatibles con la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-292">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="670a6-293">Es necesaria una cadena para el único parámetro, _version_.</span><span class="sxs-lookup"><span data-stu-id="670a6-293">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="670a6-294">Cuando la aplicación de Office llama al método **GetSupportedFeatures**, el método devuelve un valor de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="670a6-294">When the Office application calls the **GetSupportedFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="670a6-295">El valor devuelto especifica las capacidades del cliente de MI, donde cada función de la aplicación cliente de MI se indica en la aplicación de Office mediante la adición de un marcador al valor.</span><span class="sxs-lookup"><span data-stu-id="670a6-295">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="670a6-296">Las aplicaciones de Office 2013 (y siguientes) ignoran las siguientes constantes en la enumeración **OIFeature**:</span><span class="sxs-lookup"><span data-stu-id="670a6-296">Office 2013 (and higher) applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="670a6-297">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="670a6-297">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="670a6-298">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="670a6-298">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="670a6-299">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="670a6-299">**oiFeaturePhoneNormalization**</span></span>
>
>  <span data-ttu-id="670a6-300">Las aplicaciones de Office 365 versión 2011 (y siguientes) ignoran las siguientes constantes en la enumeración **OIFeature** enumeración:</span><span class="sxs-lookup"><span data-stu-id="670a6-300">Office 365 version 2011 (and higher) applications ignore following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="670a6-301">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="670a6-301">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="670a6-302">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="670a6-302">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="670a6-303">Usa el siguiente código de ejemplo para implementar el método **GetSupportFeatures** dentro del código de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-303">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="670a6-304">Interfaz ILyncClient</span><span class="sxs-lookup"><span data-stu-id="670a6-304">ILyncClient interface</span></span>
<span data-ttu-id="670a6-305"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-305"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span></span>

<span data-ttu-id="670a6-306">La interfaz **ILyncClient** se aplica a las funcionalidades de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-306">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="670a6-307">Expone propiedades que hacen referencia a la persona que inició sesión en la aplicación (usuario local, representado por la interfaz [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), el estado de la aplicación, la lista de contactos del usuario local y otras configuraciones.</span><span class="sxs-lookup"><span data-stu-id="670a6-307">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="670a6-308">Cuando está intentando conectarse a la aplicación cliente de MI, la aplicación de Office obtiene una referencia a un objeto que implementa la interfaz **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="670a6-308">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="670a6-309">Desde esa referencia, Office puede acceder a muchas de las funciones de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-309">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="670a6-310">Además, la clase que implementa la interfaz **ILyncClient** también debe implementar la interfaz **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="670a6-310">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="670a6-311">La interfaz **_ILyncClientEvents** expone muchos de los eventos que son necesarios para supervisar el estado de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-311">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="670a6-312">La Tabla 3 muestra los miembros que deben implementarse en la clase que hereda de **ILyncClient** y **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="670a6-312">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-313">Cualquier miembro de la interfaz **ILyncClient** o **\_ILyncClientEvents** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-313">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-314">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-314">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="670a6-315">Para más información sobre las interfaces **ILyncClient** y **_ILyncClientEvents** y sus miembros, consulta [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) y [ UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="670a6-315">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="670a6-316">**Tabla 3. Implementación de interfaces ILyncClient e ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="670a6-316">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="670a6-317">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="670a6-317">**Interface**</span></span>|<span data-ttu-id="670a6-318">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-318">**Member**</span></span>|<span data-ttu-id="670a6-319">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-319">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="670a6-320">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="670a6-320">**ILyncClient**</span></span> <br/> |<span data-ttu-id="670a6-321">Propiedad **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="670a6-321">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="670a6-322">Obtiene el administrador de grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="670a6-322">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="670a6-323">Propiedad **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="670a6-323">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="670a6-324">Obtiene el administrador de conversación.</span><span class="sxs-lookup"><span data-stu-id="670a6-324">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="670a6-325">Propiedad **Self**</span><span class="sxs-lookup"><span data-stu-id="670a6-325">**Self** property</span></span>  <br/> |<span data-ttu-id="670a6-326">Obtiene el objeto **Self**.</span><span class="sxs-lookup"><span data-stu-id="670a6-326">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="670a6-327">Método **SignIn**</span><span class="sxs-lookup"><span data-stu-id="670a6-327">**SignIn** method</span></span>  <br/> |<span data-ttu-id="670a6-328">Inicia el proceso de inicio de sesión de la aplicación cliente de MI con una disponibilidad específica.</span><span class="sxs-lookup"><span data-stu-id="670a6-328">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="670a6-329">Propiedad **State**</span><span class="sxs-lookup"><span data-stu-id="670a6-329">**State** property</span></span>  <br/> |<span data-ttu-id="670a6-330">Obtiene el estado actual de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="670a6-330">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="670a6-331">Propiedad **Uri**</span><span class="sxs-lookup"><span data-stu-id="670a6-331">**Uri** property</span></span>  <br/> |<span data-ttu-id="670a6-332">Obtiene el URI de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-332">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="670a6-333">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="670a6-333">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="670a6-334">Evento **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="670a6-334">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="670a6-335">Se produce cuando cambia el estado de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-335">Raised when the IM client application state changes.</span></span> <span data-ttu-id="670a6-336">Debes controlar este evento y obtener la propiedad **eventData.NewState**.</span><span class="sxs-lookup"><span data-stu-id="670a6-336">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="670a6-337">Se produce el evento para todos los procesos vinculados a una instancia de una aplicación cliente de MI cuando cualquier subsistema de la aplicación hace que cambie el estado.</span><span class="sxs-lookup"><span data-stu-id="670a6-337">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="670a6-338">Durante el proceso de inicialización, Office obtiene acceso a la propiedad **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="670a6-338">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="670a6-339">Esta propiedad debe devolver un valor de la enumeración [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState).</span><span class="sxs-lookup"><span data-stu-id="670a6-339">This property needs to return a value from the [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
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

<span data-ttu-id="670a6-340">La propiedad **State** almacena el estado actual de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-340">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="670a6-341">Se debe establecer y actualizar durante la sesión de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-341">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="670a6-342">Cuando la aplicación cliente de MI inicia sesión, cierra sesión o se apaga, debe establecer la propiedad **State**.</span><span class="sxs-lookup"><span data-stu-id="670a6-342">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="670a6-343">Es mejor establecer esta propiedad dentro de los métodos **ILyncClient.SignIn** y **ILyncClient.SignOut**, como demuestra el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="670a6-343">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
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

<span data-ttu-id="670a6-344">En el siguiente ejemplo de código se muestra cómo configurar la escucha de eventos con las interfaces _ **ILyncClientEvents** y _ **IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="670a6-344">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
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

### <a name="iautomation-interface"></a><span data-ttu-id="670a6-345">Interfaz IAutomation</span><span class="sxs-lookup"><span data-stu-id="670a6-345">IAutomation interface</span></span>
<span data-ttu-id="670a6-346"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-346"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span></span>

<span data-ttu-id="670a6-347">La interfaz **IAutomation** automatiza características de la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-347">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="670a6-348">Puedes usarla para iniciar conversaciones, unirte a conferencias y proporcionar contexto de la ventana de extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="670a6-348">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="670a6-349">La Tabla 4 muestra los miembros que deben implementarse en la clase que hereda de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="670a6-349">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-350">Cualquier miembro de la interfaz **IAutomation**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-350">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-351">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-351">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="670a6-352">Para más información sobre la interfaz **IAutomation** y sus miembros, consulta [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="670a6-352">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="670a6-353">**Tabla 4. Implementación de interfaz IAutomation**</span><span class="sxs-lookup"><span data-stu-id="670a6-353">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="670a6-354">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-354">**Member**</span></span>|<span data-ttu-id="670a6-355">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-355">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-356">Método **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="670a6-356">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="670a6-357">Inicia una conversación con la modalidad de conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="670a6-357">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="670a6-358">Se devuelve una instancia de **IConversationWindow**.</span><span class="sxs-lookup"><span data-stu-id="670a6-358">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="670a6-359">Implementar la integración de presencia de los contactos</span><span class="sxs-lookup"><span data-stu-id="670a6-359">Implementing contact presence integration</span></span>
<span data-ttu-id="670a6-360"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-360"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span></span>

<span data-ttu-id="670a6-361">Además de las tres interfaces necesarias descritas anteriormente, hay varias otras interfaces que son importantes para habilitar la funcionalidad de presencia de los contactos en Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-361">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="670a6-362">Entre ellas se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="670a6-362">These include the following:</span></span>
  
- <span data-ttu-id="670a6-363">La interfaz de [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) o **IContact2**.</span><span class="sxs-lookup"><span data-stu-id="670a6-363">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="670a6-364">La interfaz [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="670a6-364">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="670a6-365">Las interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) y [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager).</span><span class="sxs-lookup"><span data-stu-id="670a6-365">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="670a6-366">Las interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) y [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup).</span><span class="sxs-lookup"><span data-stu-id="670a6-366">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="670a6-367">La interfaz [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="670a6-367">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="670a6-368">La interfaz [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint).</span><span class="sxs-lookup"><span data-stu-id="670a6-368">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="670a6-369">La interfaz [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="670a6-369">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="670a6-370">Interfaz IContact</span><span class="sxs-lookup"><span data-stu-id="670a6-370">IContact interface</span></span>
<span data-ttu-id="670a6-371"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-371"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span></span>

<span data-ttu-id="670a6-372">La interfaz **IContact** representa un usuario de una aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-372">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="670a6-373">La interfaz expone propiedades de presencia, modalidades disponibles, pertenencia a un grupo y tipo de contacto para un usuario.</span><span class="sxs-lookup"><span data-stu-id="670a6-373">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="670a6-374">Para iniciar una conversación con otro usuario, necesitas especificar esa instancia de usuario de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="670a6-374">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="670a6-375">La Tabla 5 muestra los miembros que deben implementarse en la clase que hereda de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="670a6-375">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-376">Cualquier miembro de la interfaz **IContact**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-376">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-377">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-377">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="670a6-378">Para más información sobre la interfaz **IContact** y sus miembros, consulta [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="670a6-378">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="670a6-379">**Tabla 5. Implementación de interfaz IContact**</span><span class="sxs-lookup"><span data-stu-id="670a6-379">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="670a6-380">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-380">**Member**</span></span>|<span data-ttu-id="670a6-381">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-381">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-382">Método **CanStart**</span><span class="sxs-lookup"><span data-stu-id="670a6-382">**CanStart** method</span></span>  <br/> |<span data-ttu-id="670a6-383">Devuelve **true** si se puede iniciar un determinado tipo de modalidad en el contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-383">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="670a6-384">Método **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="670a6-384">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="670a6-385">Obtiene un elemento de la presencia de un contacto de publicación.</span><span class="sxs-lookup"><span data-stu-id="670a6-385">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="670a6-386">Método **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="670a6-386">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="670a6-387">Obtiene un elemento de presencia de un contacto de publicación.</span><span class="sxs-lookup"><span data-stu-id="670a6-387">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="670a6-388">Propiedad **Configuración**</span><span class="sxs-lookup"><span data-stu-id="670a6-388">**Settings** property</span></span>  <br/> |<span data-ttu-id="670a6-389">Obtiene una colección de propiedades del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-389">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="670a6-390">Propiedad **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="670a6-390">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="670a6-391">Obtiene una colección de grupos de los que el contacto es miembro.</span><span class="sxs-lookup"><span data-stu-id="670a6-391">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="670a6-392">Durante el proceso de inicialización, la aplicación de Office llama al método **IContact.CanStart** para determinar las funcionalidades de MI para el usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-392">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="670a6-393">El método **CanStart** toma una marca de la enumeración [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como argumento para el parámetro _ _modalityTypes_.</span><span class="sxs-lookup"><span data-stu-id="670a6-393">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  _ _modalityTypes_ parameter.</span></span> <span data-ttu-id="670a6-394">Si el usuario actual puede participar en la modalidad solicitada (es decir, el usuario puede utilizar mensajería instantánea, mensajes de audio y video y uso compartido de aplicaciones), el método **CanStart** devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="670a6-394">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
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

<span data-ttu-id="670a6-395">El método **GetContactInformation** recupera información sobre el contacto del objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="670a6-395">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="670a6-396">El código de llamada debe pasar un valor de la enumeración [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para el parámetro _ _contactInformationType_, que indica los datos que se deben recuperar.</span><span class="sxs-lookup"><span data-stu-id="670a6-396">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  _ _contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
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

<span data-ttu-id="670a6-397">Similar al método **GetContactInformation**, el método **BatchGetContactInformation** recupera varios elementos de presencia sobre el contacto del objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="670a6-397">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="670a6-398">El código de llamada debe pasar de una matriz de valores de la enumeración **ContactInformationType** para el parámetro _ _contactInformationTypes_.</span><span class="sxs-lookup"><span data-stu-id="670a6-398">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  _ _contactInformationTypes_ parameter.</span></span> <span data-ttu-id="670a6-399">El método devuelve un objeto [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="670a6-399">The method returns an [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
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

<span data-ttu-id="670a6-400">La propiedad **IContact.Settings** devuelve un objeto **IContactSettingDictionary** que contiene las propiedades personalizadas sobre el contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-400">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
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

<span data-ttu-id="670a6-401">La propiedad **IContact.CustomGroups** devuelve un objeto **IGroupCollection** que incluye todos los grupos de los que el contacto es miembro.</span><span class="sxs-lookup"><span data-stu-id="670a6-401">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
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

### <a name="iself-interface"></a><span data-ttu-id="670a6-402">Interfaz ISelf</span><span class="sxs-lookup"><span data-stu-id="670a6-402">ISelf interface</span></span>
<span data-ttu-id="670a6-403"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-403"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span></span>

<span data-ttu-id="670a6-404">Durante el proceso de inicialización, la aplicación de Office obtiene los datos del usuario actual al acceder a la propiedad **ILyncClient.Self**, que debe devolver un objeto **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="670a6-404">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="670a6-405">La interfaz **ISelf** representa al usuario de la aplicación cliente de MI conectado.</span><span class="sxs-lookup"><span data-stu-id="670a6-405">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="670a6-406">La Tabla 6 muestra los miembros que deben implementarse en la clase que hereda de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="670a6-406">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-407">Cualquier miembro de la interfaz **ISelf** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-407">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-408">Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-408">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="670a6-409">**Tabla 6. Implementación de interfaz ISelf**</span><span class="sxs-lookup"><span data-stu-id="670a6-409">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="670a6-410">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-410">**Member**</span></span>|<span data-ttu-id="670a6-411">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-411">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-412">Propiedad **Contacto**</span><span class="sxs-lookup"><span data-stu-id="670a6-412">**Contact** property</span></span>  <br/> |<span data-ttu-id="670a6-413">Obtiene el objeto **IContact** asociado con el usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-413">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="670a6-414">Las propiedades de presencia, modalidades disponibles, pertenencia a grupos y tipo de contacto del usuario local se exponen a través de la propiedad **ISelf.Contact** (que devuelve un objeto **IContact**).</span><span class="sxs-lookup"><span data-stu-id="670a6-414">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="670a6-415">Durante el proceso de inicialización, la aplicación de Office tiene acceso a la propiedad **ISelf.Contact** para obtener una referencia a la información de contacto del usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-415">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="670a6-416">Usa el código siguiente para definir una clase que hereda de la interfaz **ISelf** que implementa la propiedad **Contact**.</span><span class="sxs-lookup"><span data-stu-id="670a6-416">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
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

### <a name="icontactmanager-and-_icontactmanagerevents-interfaces"></a><span data-ttu-id="670a6-417">Las interfaces IContactManager y _IContactManagerEvents.</span><span class="sxs-lookup"><span data-stu-id="670a6-417">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="670a6-418"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-418"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span></span>

<span data-ttu-id="670a6-419">El objeto **IContactManager** administra los contactos del usuario local, con la información de contacto propia del usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-419">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="670a6-420">La aplicación de Office utiliza un objeto **IContactManager** para acceder a los objetos **IContact** que se corresponden con los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-420">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="670a6-421">La Tabla 7 muestra los miembros que deben implementarse en la clase que hereda de **IContactManager** y **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="670a6-421">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-422">Cualquier miembro de la interfaz **IContactManager** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-422">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-423">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-423">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="670a6-424">Para más información sobre las interfaces **IContactManager** y **_IContactManagerEvents** y sus miembros, consulta [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) y [ UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="670a6-424">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="670a6-425">**Tabla 7. Implementación de las interfaces IContactManager y _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="670a6-425">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="670a6-426">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="670a6-426">**Interface**</span></span>|<span data-ttu-id="670a6-427">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-427">**Member**</span></span>|<span data-ttu-id="670a6-428">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-428">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="670a6-429">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="670a6-429">**IContactManager**</span></span> <br/> |<span data-ttu-id="670a6-430">Método **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="670a6-430">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="670a6-431">Busca o crea una nueva instancia de contacto usando el URI de contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-431">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="670a6-432">Método **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="670a6-432">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="670a6-433">Crea un objeto **ISubscription** que puede usarse para suscripciones por lotes o consultas.</span><span class="sxs-lookup"><span data-stu-id="670a6-433">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="670a6-434">Método **Lookup**</span><span class="sxs-lookup"><span data-stu-id="670a6-434">**Lookup** method</span></span>  <br/> |<span data-ttu-id="670a6-435">Busca un contacto o grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="670a6-435">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="670a6-436">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="670a6-436">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="670a6-437">Evento **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="670a6-437">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="670a6-438">Se produce cuando se agrega un grupo a una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="670a6-438">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="670a6-439">La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="670a6-439">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="670a6-440">Evento **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="670a6-440">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="670a6-441">Se produce cuando se quita un grupo de una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="670a6-441">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="670a6-442">La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="670a6-442">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="670a6-443">Evento **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="670a6-443">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="670a6-444">Se produce cuando cambia el estado de un proveedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="670a6-444">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="670a6-445">Office llama a **IContactManager.GetContactByUri** para obtener información de presencia de un contacto mediante la dirección SIP del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-445">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="670a6-446">Cuando un contacto está configurado para una dirección SIP en Active Directory, Office determina esta dirección para un contacto y llama a **GetContactByUri**, al pasar la dirección SIP del contacto para el parámetro _ _contactUri_.</span><span class="sxs-lookup"><span data-stu-id="670a6-446">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  _ _contactUri_ parameter.</span></span> 
  
<span data-ttu-id="670a6-447">Cuando Office no puede determinar la dirección SIP para un contacto, llama al método **IContactManager.Lookup** para encontrar el SIP mediante el servicio de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-447">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="670a6-448">Aquí Office pasa los mejores datos que puede encontrar para el contacto (por ejemplo, solo la dirección de correo del contacto).</span><span class="sxs-lookup"><span data-stu-id="670a6-448">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="670a6-449">El método **Lookup** devuelve de forma asincrónica un objeto **AsynchronousOperation**.</span><span class="sxs-lookup"><span data-stu-id="670a6-449">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="670a6-450">Cuando invoca la retrollamada, el método **Lookup** debe devolver el éxito o fracaso de la operación además del URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-450">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
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

<span data-ttu-id="670a6-451">La aplicación de Office debe suscribirse a los cambios de presencia de un contacto individual.</span><span class="sxs-lookup"><span data-stu-id="670a6-451">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="670a6-452">Por lo tanto, cuando cambia el estado de presencia de un contacto, el servidor de MI le avisa a la aplicación cliente de MI, lo que alerta a la aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="670a6-452">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="670a6-453">Para ello, la aplicación de Office llama al método **IContactManager.CreateSubscription** para crear un nuevo objeto **IContactSubscription** para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="670a6-453">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
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

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="670a6-454">Interfaces IGroup e IGroupCollection.</span><span class="sxs-lookup"><span data-stu-id="670a6-454">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="670a6-455"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-455"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span></span>

<span data-ttu-id="670a6-456">El objeto **IGroup** representa una colección de contactos con propiedades adicionales para identificar la colección de contactos mediante un nombre de grupo colectivo.</span><span class="sxs-lookup"><span data-stu-id="670a6-456">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="670a6-457">Un objeto **IGroupCollection** representa una colección de objetos **IGroup** definidos por el usuario local y la aplicación de cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-457">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="670a6-458">La aplicación de Office usa los objetos **IGroupCollection** y **IGroup** para tener acceso a los contactos del usuario local.</span><span class="sxs-lookup"><span data-stu-id="670a6-458">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="670a6-459">La Tabla 9 muestra los miembros que deben implementarse en las clases que heredan de **IGroup** e **IGroupCollection** en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="670a6-459">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="670a6-460">Cualquier miembro de la interfaz **IGroup** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-460">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-461">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-461">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="670a6-462">Para más información sobre las interfaces **IGroup** e **IGroupCollection** y sus miembros, consulta [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) y [ UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="670a6-462">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="670a6-463">**Tabla 9. Implementación de las interfaces IGroup e IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="670a6-463">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="670a6-464">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="670a6-464">**Interface**</span></span>|<span data-ttu-id="670a6-465">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-465">**Member**</span></span>|<span data-ttu-id="670a6-466">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-466">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="670a6-467">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="670a6-467">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="670a6-468">Propiedad **Count**</span><span class="sxs-lookup"><span data-stu-id="670a6-468">**Count** property</span></span>  <br/> |<span data-ttu-id="670a6-469">Devuelve el número de objeto **IGroup** de la colección</span><span class="sxs-lookup"><span data-stu-id="670a6-469">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="670a6-470">Propiedad **Item**</span><span class="sxs-lookup"><span data-stu-id="670a6-470">**Item** property</span></span>  <br/> |<span data-ttu-id="670a6-471">Devuelve el objeto **IGroup** en el índice especificado en la colección.</span><span class="sxs-lookup"><span data-stu-id="670a6-471">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="670a6-472">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="670a6-472">**IGroup**</span></span> <br/> |<span data-ttu-id="670a6-473">Propiedad **Id**</span><span class="sxs-lookup"><span data-stu-id="670a6-473">**Id** property</span></span>  <br/> |<span data-ttu-id="670a6-474">Devuelve el id. del grupo.</span><span class="sxs-lookup"><span data-stu-id="670a6-474">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="670a6-475">Cuando la aplicación de Office obtiene la información de usuario local, tiene acceso a la pertenencia del contacto (usuario local) al llamar a la propiedad **IContact.CustomGroups** que devuelve un objeto **IGroupCollection**.</span><span class="sxs-lookup"><span data-stu-id="670a6-475">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="670a6-476">**IGroupCollection** debe contener una matriz (o **lista**) de objetos **IGroup**.</span><span class="sxs-lookup"><span data-stu-id="670a6-476">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="670a6-477">La clase que se deriva de **IGroupCollection** debe exponer una propiedad **Count**, que devuelve el número de elementos de la colección y un método indizador, **this(int)**, que devuelve un objeto **IGroup** de la colección.</span><span class="sxs-lookup"><span data-stu-id="670a6-477">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="670a6-478">Interfaz IContactSubscription.</span><span class="sxs-lookup"><span data-stu-id="670a6-478">IContactSubscription interface</span></span>
<span data-ttu-id="670a6-479"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-479"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span></span>

<span data-ttu-id="670a6-480">La interfaz **IContactSubscription** te permite especificar los contactos para recibir actualizaciones de la información de presencia y los tipos de información de presencia que activan una notificación.</span><span class="sxs-lookup"><span data-stu-id="670a6-480">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="670a6-481">Las aplicaciones de Office utilizan un objeto **IContactSubscription** para registrar cambios al estado de presencia del contacto</span><span class="sxs-lookup"><span data-stu-id="670a6-481">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="670a6-482">La Tabla 10 muestra los miembros que deben implementarse en las clases que heredan de **IContactSuscription**.</span><span class="sxs-lookup"><span data-stu-id="670a6-482">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-483">Cualquier miembro de la interfaz **IContactSubscription** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-483">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-484">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-484">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="670a6-485">Para más información sobre la interfaz **IContactSubscription** y sus miembros, consulta [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="670a6-485">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="670a6-486">**Tabla 10. Implementación de interfaz IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="670a6-486">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="670a6-487">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-487">**Member**</span></span>|<span data-ttu-id="670a6-488">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-488">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-489">Método **AddContact**</span><span class="sxs-lookup"><span data-stu-id="670a6-489">**AddContact** method</span></span>  <br/> |<span data-ttu-id="670a6-490">Agrega un contacto al objeto de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="670a6-490">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="670a6-491">Método **Subscribe**</span><span class="sxs-lookup"><span data-stu-id="670a6-491">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="670a6-492">Ayuda de la aplicación cliente de MI a supervisar la presencia de un contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-492">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="670a6-493">La interfaz **IContactSubscription** debe contener una referencia a todos los objetos **IContact** que supervisa, mediante el uso de una matriz o una **Lista**.</span><span class="sxs-lookup"><span data-stu-id="670a6-493">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="670a6-494">El método **IContactSubscription.AddContact** agrega un objeto **IContact** a la estructura de datos subyacente del objeto **IContactSubscription**, lo que agrega un contacto nuevo para supervisar los cambios de presencia.</span><span class="sxs-lookup"><span data-stu-id="670a6-494">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="670a6-495">El método **IContactSubscription.Subscribe** permite que una aplicación cliente de MI acceda a observadores de presencia del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-495">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="670a6-496">Puede usar una estrategia de sondeo para obtener la presencia del servidor de los contactos para los que se haya suscrito la aplicación cliente de MI.</span><span class="sxs-lookup"><span data-stu-id="670a6-496">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="670a6-497">El método **Subscribe** es útil en situaciones donde se solicita la presencia de alguien de fuera de la lista de contactos de un usuario (por ejemplo, de una red pública de mayor tamaño).</span><span class="sxs-lookup"><span data-stu-id="670a6-497">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="670a6-498">Interfaz IContactEndPoint.</span><span class="sxs-lookup"><span data-stu-id="670a6-498">IContactEndPoint interface</span></span>
<span data-ttu-id="670a6-499"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-499"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span></span>

<span data-ttu-id="670a6-500">**IContactEndPoint** representa un número de teléfono de la colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-500">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="670a6-501">La Tabla 11 muestra los miembros que deben implementarse en las clases que heredan de **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="670a6-501">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-502">Cualquier miembro de la interfaz **IContactEndPoint**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-502">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-503">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-503">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="670a6-504">Para más información sobre la interfaz **IContactEndPoint** y sus miembros, consulta [UCCollaborationLib.IContactEndPoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="670a6-504">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="670a6-505">**Tabla 11. Implementación de la interfaz IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="670a6-505">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="670a6-506">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-506">**Member**</span></span>|<span data-ttu-id="670a6-507">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-507">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-508">Propiedad **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="670a6-508">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="670a6-509">Obtiene la cadena para mostrar</span><span class="sxs-lookup"><span data-stu-id="670a6-509">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="670a6-510">Propiedad **Type**</span><span class="sxs-lookup"><span data-stu-id="670a6-510">**Type** property</span></span>  <br/> |<span data-ttu-id="670a6-511">Obtiene el tipo de punto de contacto</span><span class="sxs-lookup"><span data-stu-id="670a6-511">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="670a6-512">Propiedad **Uri**</span><span class="sxs-lookup"><span data-stu-id="670a6-512">**Uri** property</span></span>  <br/> |<span data-ttu-id="670a6-513">Obtiene el URI del contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-513">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="670a6-514">Interfaz ILocaleString</span><span class="sxs-lookup"><span data-stu-id="670a6-514">ILocaleString interface</span></span>
<span data-ttu-id="670a6-515"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="670a6-515"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span></span>

<span data-ttu-id="670a6-516">**ILocaleString** es una estructura de cadena localizada que contiene una cadena localizada y el ID de la localización de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="670a6-516">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="670a6-517">La interfaz **ILocaleString** se utiliza para dar formato a la cadena de estado personalizado en la tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="670a6-517">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="670a6-518">La Tabla 12 muestra los miembros que deben implementarse en las clases que heredan de **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="670a6-518">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="670a6-519">Cualquier miembro de la interfaz **ILocaleString** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo.</span><span class="sxs-lookup"><span data-stu-id="670a6-519">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="670a6-520">Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="670a6-520">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="670a6-521">Para más información sobre la interfaz **ILocaleString** y sus miembros, consulta [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="670a6-521">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="670a6-522">**Tabla 12. Implementación de interfaz ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="670a6-522">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="670a6-523">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="670a6-523">**Member**</span></span>|<span data-ttu-id="670a6-524">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="670a6-524">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="670a6-525">Propiedad **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="670a6-525">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="670a6-526">Obtiene la id. de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="670a6-526">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="670a6-527">Propiedad **Value**</span><span class="sxs-lookup"><span data-stu-id="670a6-527">**Value** property</span></span>  <br/> |<span data-ttu-id="670a6-528">Obtiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="670a6-528">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="670a6-529">Ver también</span><span class="sxs-lookup"><span data-stu-id="670a6-529">See also</span></span>

- <span data-ttu-id="670a6-530">Espacio de nombre [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="670a6-530">[UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

