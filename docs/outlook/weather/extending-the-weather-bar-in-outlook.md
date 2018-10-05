---
title: Ampliación de la barra de meteorología en Outlook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b355b98-dd7d-4f16-8257-367e5dd61b34
description: Obtenga información sobre cómo conectar un servicio web de meteorología de terceros para la barra de meteorología en Outlook 2013, para proporcionar datos de las condiciones de tiempo para una ubicación elegido por el usuario.
ms.openlocfilehash: 0423e149306bf7562dd525f1b7460a63cbace372
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386582"
---
# <a name="extending-the-weather-bar-in-outlook"></a><span data-ttu-id="86745-103">Ampliación de la barra de meteorología en Outlook</span><span class="sxs-lookup"><span data-stu-id="86745-103">Extending the Weather Bar in Outlook</span></span>

<span data-ttu-id="86745-104">Obtenga información sobre cómo conectar un servicio web de meteorología de terceros para la barra de meteorología en Outlook 2013, para proporcionar datos de las condiciones de tiempo para una ubicación elegido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="86745-104">Learn how to plug in a third-party weather web service for the Weather Bar in Outlook 2013, to provide weather conditions data for a user-chosen location.</span></span>
  
## <a name="weather-bar-overview"></a><span data-ttu-id="86745-105">Introducción a la barra de meteorología</span><span class="sxs-lookup"><span data-stu-id="86745-105">Weather Bar overview</span></span>
<span data-ttu-id="86745-106"><a name="ol15_weatherbar_overview"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-106"></span></span>

<span data-ttu-id="86745-p101">La barra de meteorología en Outlook muestra las condiciones de meteorología y previsión para una ubicación geográfica. Un usuario puede elegir una o varias ubicaciones y ver fácilmente datos de tiempo en la barra de meteorología en el módulo calendario. La figura 1 muestra la barra de meteorología mostrar una previsión de tres días para Nueva York, NY.</span><span class="sxs-lookup"><span data-stu-id="86745-p101">The Weather Bar in Outlook displays weather conditions and forecast for a geographic location. A user can choose one or multiple locations, and conveniently see weather data in the Weather Bar in the calendar module. Figure 1 shows the Weather Bar displaying a three-day forecast for New York, NY.</span></span> 
  
<span data-ttu-id="86745-110">**En la figura 1. Barra de meteorología de Outlook**</span><span class="sxs-lookup"><span data-stu-id="86745-110">**Figure 1. Weather Bar in Outlook**</span></span>

![Barra de tiempo con la previsión para Nueva York](media/ol15_WeatherBar_fig1.jpg)
  
<span data-ttu-id="86745-p102">Configuración de la barra de meteorología se guarda con el perfil del usuario. Según el tipo de cuenta de Outlook, la configuración puede variar con el usuario en todos los equipos a los que el usuario inicia sesión con el mismo perfil, como en el caso de cuentas de Exchange. Como alternativa, el usuario puede personalizar la configuración en cada equipo, como en el caso de las cuentas IMAP o POP.</span><span class="sxs-lookup"><span data-stu-id="86745-p102">Settings for the Weather Bar are saved with the user's profile. Depending on the type of Outlook account, the settings may roam with the user on all computers that the user logs on to with the same profile, as in the case of Exchange accounts. Alternatively, the user can customize settings on each computer, as in the case of IMAP/POP accounts.</span></span>
  
<span data-ttu-id="86745-p103">De forma predeterminada, Outlook utiliza datos de tiempo proporcionados por MSN el tiempo. La barra de meteorología admite servicios de web de datos de tiempo de otro fabricante que seguir un protocolo definido para comunicarse con Outlook. Como un servicio de datos de tiempo de terceros compatible con este protocolo, los usuarios pueden elegir ese servicio de información meteorológica para proporcionar datos de tiempo en la barra de meteorología. En este artículo se describe el protocolo de servicios de tiempo de terceros que se integra con Outlook en la barra de meteorología.</span><span class="sxs-lookup"><span data-stu-id="86745-p103">By default, Outlook uses weather data provided by MSN Weather. The Weather Bar supports third-party weather data web services that follow a defined protocol to communicate with Outlook. As long as a third-party weather data service supports this protocol, users can choose that weather data service to provide weather data in the Weather Bar. This article describes the protocol for third-party weather services to integrate with Outlook in the Weather Bar.</span></span>
  
## <a name="weather-bar-protocol"></a><span data-ttu-id="86745-119">Protocolo de barra de meteorología</span><span class="sxs-lookup"><span data-stu-id="86745-119">Weather Bar protocol</span></span>
<span data-ttu-id="86745-120"><a name="ol15_weatherbar_theprotocol"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-120"></span></span>

<span data-ttu-id="86745-121">Un usuario puede especificar un servicio de datos de tiempo diferente para la barra de meteorología, siempre y cuando ese servicio de información meteorológica implementa un servicio web que admite el protocolo para comunicarse con Outlook siguiente:</span><span class="sxs-lookup"><span data-stu-id="86745-121">A user can specify a different weather data service for the Weather Bar, as long as that weather data service implements a web service that supports the following protocol to communicate with Outlook:</span></span>
  
1. <span data-ttu-id="86745-p104">El servicio de información meteorológica admite una dirección URL base a un servicio web. Por ejemplo, un servicio web meteorológico de Contoso puede tener una dirección URL base de https://service.contoso.com/data.aspx.</span><span class="sxs-lookup"><span data-stu-id="86745-p104">The weather data service supports a base URL to a web service. For example, a Contoso Weather web service can have a base URL of https://service.contoso.com/data.aspx.</span></span>
    
2. <span data-ttu-id="86745-124">El servicio web permite Outlook anexar los siguientes parámetros a la dirección URL base, para solicitar un código de ubicación:</span><span class="sxs-lookup"><span data-stu-id="86745-124">The web service allows Outlook to append the following parameters to the base URL, to request a location code:</span></span> 
    
   - <span data-ttu-id="86745-125">outputview = búsqueda: este parámetro indica que la solicitud es una búsqueda de ubicación.</span><span class="sxs-lookup"><span data-stu-id="86745-125">outputview=search: This parameter indicates that the request is a location search.</span></span>
    
   - <span data-ttu-id="86745-126">weasearchstr = _Ciudad_: este parámetro indica la ubicación, _Ciudad_, para que el usuario desea una previsión meteorológica (por ejemplo, London).</span><span class="sxs-lookup"><span data-stu-id="86745-126">weasearchstr= _city_: This parameter indicates the location,  _city_, for which the user wants a weather forecast (for example, London).</span></span>
    
   - <span data-ttu-id="86745-127">referencia cultural = _LCID_: este parámetro indica la referencia cultural de la versión de Office instalada para el usuario en dicho equipo.</span><span class="sxs-lookup"><span data-stu-id="86745-127">culture= _LCID_: This parameter indicates the culture of the version of Office installed for the user on that computer.</span></span> <span data-ttu-id="86745-128">El valor de LCID se define en [etiquetas de [RFC4646] para identificar los idiomas](https://www.ietf.org/rfc/rfc4646.txt)</span><span class="sxs-lookup"><span data-stu-id="86745-128">The LCID value is defined in [[RFC4646] Tags for Identifying Languages](https://www.ietf.org/rfc/rfc4646.txt)</span></span>
    
   - <span data-ttu-id="86745-129">src = outlook: este parámetro indica que Outlook es la aplicación de cliente que solicita el servicio.</span><span class="sxs-lookup"><span data-stu-id="86745-129">src=outlook: This parameter indicates that Outlook is the client application requesting the service.</span></span>
    
   <span data-ttu-id="86745-p106">Estos parámetros permiten Outlook para tomar la ubicación que el usuario está interesado en y busque el código de ubicación asociada según la compatibilidad con el servicio de información meteorológica. El servicio web debe responder a Outlook con un código de ubicación en XML que sigue a la [Outlook Weather Location XML Schema](outlook-weather-location-xml-schema.md). La figura 2 se resume la solicitud de servicio web y la respuesta para un código de ubicación.</span><span class="sxs-lookup"><span data-stu-id="86745-p106">These parameters allow Outlook to take the location that the user is interested in and search for the associated location code as supported by the weather data service. The web service should respond to Outlook with a location code in XML that follows the [Outlook Weather Location XML Schema](outlook-weather-location-xml-schema.md). Figure 2 summarizes the web service request and response for a location code.</span></span>
    
   <span data-ttu-id="86745-133">**La figura 2. Solicitud de servicio Web y la respuesta para un código de ubicación**</span><span class="sxs-lookup"><span data-stu-id="86745-133">**Figure 2. Web service request and response for a location code**</span></span>

   ![Solicitud y respuesta de ubicación de tiempo](media/ol15_WeatherBar_Fig02.gif)
  
3. <span data-ttu-id="86745-135">El servicio web también permite Outlook anexar los siguientes parámetros, para solicitar información de previsión para un código de ubicación:</span><span class="sxs-lookup"><span data-stu-id="86745-135">The web service also allows Outlook to append the following parameters, to request forecast information for a location code:</span></span>
    
   - <span data-ttu-id="86745-136">wealocations = _código_: _código_ en este parámetro es un código de ubicación que Outlook se obtiene del paso 2, y que se asigna a la ubicación que el usuario está interesado en.</span><span class="sxs-lookup"><span data-stu-id="86745-136">wealocations= _code_: _code_ in this parameter is a location code that Outlook obtains from Step 2, and that maps to the location that the user is interested in.</span></span> 
    
   - <span data-ttu-id="86745-137">weadegreetype = _degreetype_: este parámetro especifica si se usa el sistema métrico o imperial unidades de medida de temperatura.</span><span class="sxs-lookup"><span data-stu-id="86745-137">weadegreetype= _degreetype_: This parameter specifies whether to use metric or imperial units of measurement for temperature.</span></span> <span data-ttu-id="86745-138">Especificar c de métrica, f para imperial para  _degreetype_.</span><span class="sxs-lookup"><span data-stu-id="86745-138">Specify c for metric, f for imperial for  _degreetype_.</span></span> <span data-ttu-id="86745-139">Este parámetro es opcional y no siempre se encuentra en la solicitud de servicio web.</span><span class="sxs-lookup"><span data-stu-id="86745-139">This parameter is optional and does not always exist in the web service request.</span></span>
    
   - <span data-ttu-id="86745-140">referencia cultural = _LCID_: este parámetro indica la referencia cultural de la versión de Office instalada para el usuario en dicho equipo.</span><span class="sxs-lookup"><span data-stu-id="86745-140">culture= _LCID_: This parameter indicates the culture of the version of Office installed for the user on that computer.</span></span> <span data-ttu-id="86745-141">El valor de LCID se define en [etiquetas de [RFC4646] para identificar los idiomas](https://www.ietf.org/rfc/rfc4646.txt)</span><span class="sxs-lookup"><span data-stu-id="86745-141">The LCID value is defined in [[RFC4646] Tags for Identifying Languages](https://www.ietf.org/rfc/rfc4646.txt)</span></span>
    
   - <span data-ttu-id="86745-142">src = outlook: este parámetro indica que Outlook es la aplicación de cliente que solicita el servicio.</span><span class="sxs-lookup"><span data-stu-id="86745-142">src=outlook: This parameter indicates that Outlook is the client application requesting the service.</span></span>
    
   <span data-ttu-id="86745-p109">Estos parámetros permiten Outlook tomar el código de ubicación devuelto del paso 2 y solicitan el servicio de información meteorológica para la previsión. El servicio web debe responder a Outlook con los datos de tiempo correspondiente en XML que sigue a la [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md). La figura 3 se resume la solicitud de servicio web y la respuesta para los datos de tiempo dado un código de ubicación.</span><span class="sxs-lookup"><span data-stu-id="86745-p109">These parameters allow Outlook to take the location code returned from Step 2 and request the weather data service for the forecast. The web service should respond to Outlook with the corresponding weather data in XML that follows the [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md). Figure 3 summarizes the web service request and response for weather data given a location code.</span></span>
    
   <span data-ttu-id="86745-146">**La figura 3. Solicitud de servicio Web y la respuesta de información meteorológica**</span><span class="sxs-lookup"><span data-stu-id="86745-146">**Figure 3. Web service request and response for weather information**</span></span>

   ![Solicitud y respuesta de información de tiempo](media/ol15_WeatherBar_Fig03.gif)
  
## <a name="setting-the-weather-bar-to-use-a-weather-service"></a><span data-ttu-id="86745-148">Configuración de la barra de meteorología para usar un servicio meteorológico</span><span class="sxs-lookup"><span data-stu-id="86745-148">Setting the Weather Bar to use a weather service</span></span>
<span data-ttu-id="86745-149"><a name="ol15_weatherbar_setting"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-149"></span></span>

<span data-ttu-id="86745-p110">El administrador o usuario avanzado puede usar la clave del registro de **WeatherServiceUrl** para personalizar la barra de meteorología para usar un servicio de tiempo específico. Por ejemplo, si la dirección URL base para un servicio meteorológico de Contoso es https://service.contoso.com/data.aspx, puede establecer la clave de **WeatherServiceUrl** en esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="86745-p110">The administrator or power user can use the **WeatherServiceUrl** registry key to customize the Weather Bar to use a specific weather service. For example, if the base URL for a Contoso weather service is https://service.contoso.com/data.aspx, you can set the **WeatherServiceUrl** key to that URL.</span></span> 
  
<span data-ttu-id="86745-152">En la siguiente tabla describe la clave **WeatherServiceUrl**.</span><span class="sxs-lookup"><span data-stu-id="86745-152">The following table describes the **WeatherServiceUrl** key.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86745-153">**Clave**</span><span class="sxs-lookup"><span data-stu-id="86745-153">**Key**</span></span> <br/> |<span data-ttu-id="86745-154">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span><span class="sxs-lookup"><span data-stu-id="86745-154">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span></span>  <br/> |
|<span data-ttu-id="86745-155">**Nombre del valor**</span><span class="sxs-lookup"><span data-stu-id="86745-155">**Value name**</span></span> <br/> |<span data-ttu-id="86745-156">**WeatherServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="86745-156">**WeatherServiceUrl**</span></span> <br/> |
|<span data-ttu-id="86745-157">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="86745-157">**Value type**</span></span> <br/> |<span data-ttu-id="86745-158">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="86745-158">REG_SZ</span></span>  <br/> |
|<span data-ttu-id="86745-159">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="86745-159">**Default value**</span></span> <br/> |<span data-ttu-id="86745-160">EMPTY_STRING</span><span class="sxs-lookup"><span data-stu-id="86745-160">EMPTY_STRING</span></span>  <br/> |
|<span data-ttu-id="86745-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86745-161">**Description**</span></span> <br/> |<span data-ttu-id="86745-162">Dirección URL de un servicio de información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="86745-162">URL to a weather data service.</span></span>  <br/> |
   
## <a name="dependent-conditions"></a><span data-ttu-id="86745-163">Condiciones dependientes</span><span class="sxs-lookup"><span data-stu-id="86745-163">Dependent conditions</span></span>
<span data-ttu-id="86745-164"><a name="ol15_weatherbar_dependentconditions"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-164"></span></span>

<span data-ttu-id="86745-p111">Outlook 2013 muestra la barra de meteorología de forma predeterminada. Esta sección describen algunos motivos por los que la barra de meteorología puede no ser visible.</span><span class="sxs-lookup"><span data-stu-id="86745-p111">Outlook 2013 displays the Weather Bar by default. This section describes a few reasons why the Weather Bar might not be visible.</span></span>
  
### <a name="weather-bar-is-disabled"></a><span data-ttu-id="86745-167">Se deshabilita la barra de meteorología</span><span class="sxs-lookup"><span data-stu-id="86745-167">Weather Bar is disabled</span></span>

<span data-ttu-id="86745-168">En primer lugar, compruebe que la opción **Mostrar el tiempo en el calendario** esté seleccionado en la ficha de **calendario** en el cuadro de diálogo **Opciones de Outlook**.</span><span class="sxs-lookup"><span data-stu-id="86745-168">First, verify that **Show weather on the calendar** is selected in the **Calendar** tab in the **Outlook Options** dialog box.</span></span> 
  
<span data-ttu-id="86745-169">Tenga en cuenta que un administrador también puede usar Directiva de grupo para deshabilitar la barra de meteorología en Outlook 2013 totalmente estableciendo la siguiente clave del registro de Windows:</span><span class="sxs-lookup"><span data-stu-id="86745-169">Note that an administrator can also use Group Policy to disable the Weather Bar in Outlook 2013 entirely by setting the following key in the Windows registry:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86745-170">**Clave**</span><span class="sxs-lookup"><span data-stu-id="86745-170">**Key**</span></span> <br/> |<span data-ttu-id="86745-171">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span><span class="sxs-lookup"><span data-stu-id="86745-171">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span></span>  <br/> |
|<span data-ttu-id="86745-172">**Nombre del valor**</span><span class="sxs-lookup"><span data-stu-id="86745-172">**Value name**</span></span> <br/> |<span data-ttu-id="86745-173">**DisableWeather**</span><span class="sxs-lookup"><span data-stu-id="86745-173">**DisableWeather**</span></span> <br/> |
|<span data-ttu-id="86745-174">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="86745-174">**Value type**</span></span> <br/> |<span data-ttu-id="86745-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="86745-175">REG_DWORD</span></span>  <br/> |
|<span data-ttu-id="86745-176">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="86745-176">**Default value**</span></span> <br/> |<span data-ttu-id="86745-177">0</span><span class="sxs-lookup"><span data-stu-id="86745-177">0</span></span>  <br/> |
|<span data-ttu-id="86745-178">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86745-178">**Description**</span></span> <br/> |<span data-ttu-id="86745-179">Un valor de 0 permite la barra de meteorología; cualquier otro valor, deshabilita la barra de meteorología.</span><span class="sxs-lookup"><span data-stu-id="86745-179">A value of 0 enables the Weather Bar; any other value disables the Weather Bar.</span></span>  <br/> |
   
<span data-ttu-id="86745-p112">Si se ha deshabilitado la característica de barra de meteorología mediante la directiva de grupo, la ficha **calendario** no incluye la casilla de verificación **Mostrar el tiempo en el calendario**. Póngase en contacto con el administrador para volver a activar la característica.</span><span class="sxs-lookup"><span data-stu-id="86745-p112">If the Weather Bar feature has been disabled by Group Policy, the **Calendar** tab does not include the **Show weather on the calendar** check box. Consult with the administrator to turn the feature back on.</span></span> 
  
### <a name="office-is-disconnected-from-the-internet"></a><span data-ttu-id="86745-182">Office se desconecta de Internet</span><span class="sxs-lookup"><span data-stu-id="86745-182">Office is disconnected from the Internet</span></span>

<span data-ttu-id="86745-183">Comprobar que Office está habilitado para conectarse a Internet, vaya a la ficha **Opciones de privacidad** del **Centro de confianza** en la vista Backstage y a continuación, asegúrese de que esté seleccionado **Permitir Office para conectarse a Internet**.</span><span class="sxs-lookup"><span data-stu-id="86745-183">Verify that Office is enabled to connect to the Internet—go to the **Privacy options** tab of the **Trust Center** in the Backstage view, and ensure that **Allow Office to connect to the Internet** is selected.</span></span> 
  
<span data-ttu-id="86745-184">Si el usuario ha decidido no recibir actualizaciones para Office, la barra de meteorología también está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="86745-184">If the user has chosen to not receive updates for Office, the Weather Bar is also disabled.</span></span>
  
<span data-ttu-id="86745-185">Un administrador también puede usar la directiva de grupo para deshabilitar todo el contenido en línea, incluida la barra de meteorología, estableciendo la siguiente clave del registro de Windows:</span><span class="sxs-lookup"><span data-stu-id="86745-185">An administrator can also use Group Policy to disable all online content, including the Weather Bar, by setting the following key in the Windows registry:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86745-186">**Clave**</span><span class="sxs-lookup"><span data-stu-id="86745-186">**Key**</span></span> <br/> |<span data-ttu-id="86745-187">HKCU\Software\Microsoft\Office\15.0\Common\Internet</span><span class="sxs-lookup"><span data-stu-id="86745-187">HKCU\Software\Microsoft\Office\15.0\Common\Internet</span></span>  <br/> |
|<span data-ttu-id="86745-188">**Nombre del valor**</span><span class="sxs-lookup"><span data-stu-id="86745-188">**Value name**</span></span> <br/> |<span data-ttu-id="86745-189">**UseOnlineContent**</span><span class="sxs-lookup"><span data-stu-id="86745-189">**UseOnlineContent**</span></span> <br/> |
|<span data-ttu-id="86745-190">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="86745-190">**Value type**</span></span> <br/> |<span data-ttu-id="86745-191">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="86745-191">REG_DWORD</span></span>  <br/> |
|<span data-ttu-id="86745-192">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="86745-192">**Default value**</span></span> <br/> |<span data-ttu-id="86745-193">2</span><span class="sxs-lookup"><span data-stu-id="86745-193">2</span></span>  <br/> |
|<span data-ttu-id="86745-194">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86745-194">**Description**</span></span> <br/> |<span data-ttu-id="86745-195">El valor 2 habilita la barra de meteorología; cualquier otro valor, deshabilita la barra de meteorología.</span><span class="sxs-lookup"><span data-stu-id="86745-195">A value of 2 enables the Weather Bar; any other value disables the Weather Bar.</span></span>  <br/> |
   
<span data-ttu-id="86745-p113">Si se ha deshabilitado la característica de barra de meteorología mediante la directiva de grupo, la ficha **calendario** no incluye la casilla de verificación **Mostrar el tiempo en el calendario**. Póngase en contacto con el administrador para volver a activar la característica.</span><span class="sxs-lookup"><span data-stu-id="86745-p113">If the Weather Bar feature has been disabled by Group Policy, the **Calendar** tab does not include the **Show weather on the calendar** check box. Consult with the administrator to turn the feature back on.</span></span> 
  
## <a name="weather-bar-example"></a><span data-ttu-id="86745-198">Ejemplo de barra de meteorología</span><span class="sxs-lookup"><span data-stu-id="86745-198">Weather Bar example</span></span>
<span data-ttu-id="86745-199"><a name="ol15_weatherbar_example"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-199"></span></span>

<span data-ttu-id="86745-p114">En esta sección se muestra un ejemplo de un servicio meteorológico de Contoso que sigue el protocolo anterior para comunicarse con Outlook. Para cualquier ubicación que el usuario selecciona, Outlook obtiene primero un código de ubicación para la ubicación de meteorología de Contoso, a continuación, usar ese código de ubicación, llama al servicio de tiempo de Contoso para obtener los datos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="86745-p114">This section shows an example of a Contoso Weather service that follows the preceding protocol to communicate with Outlook. For any location that the user selects, Outlook first gets a location code for that location from Contoso Weather, then using that location code, calls the Contoso Weather service to get the weather data.</span></span>
  
### <a name="base-url"></a><span data-ttu-id="86745-202">dirección URL base</span><span class="sxs-lookup"><span data-stu-id="86745-202">Base URL</span></span>

<span data-ttu-id="86745-203">Tiempo de Contoso proporciona la siguiente dirección URL base para su servicio de información meteorológica:</span><span class="sxs-lookup"><span data-stu-id="86745-203">Contoso Weather provides the following base URL for their weather data service:</span></span>
  
https://service.contoso.com/data.aspx
  
### <a name="getting-a-location-code"></a><span data-ttu-id="86745-204">Obtención de un código de ubicación</span><span class="sxs-lookup"><span data-stu-id="86745-204">Getting a location code</span></span>

<span data-ttu-id="86745-205">Outlook anexa los parámetros descritos en el paso 2 anterior a la dirección URL base para obtener el código de ubicación para una ubicación geográfica  _city_:</span><span class="sxs-lookup"><span data-stu-id="86745-205">Outlook appends the parameters described in Step 2 above to the base URL to obtain the location code for a geographic location  _city_:</span></span>
  
<span data-ttu-id="86745-206">https://service.contoso.com/data.aspx?outputview=search&amp;weasearchstr= _city_</span><span class="sxs-lookup"><span data-stu-id="86745-206">https://service.contoso.com/data.aspx?outputview=search&amp;weasearchstr= _city_</span></span>
  
<span data-ttu-id="86745-207">Por ejemplo, si el usuario ha seleccionado Tokio en la barra de meteorología, Outlook utiliza la siguiente dirección URL para obtener el código de ubicación de Tokio de meteorología de Contoso:</span><span class="sxs-lookup"><span data-stu-id="86745-207">As an example, if the user has selected Tokyo in the Weather Bar, Outlook uses the following URL to obtain the location code for Tokyo from Contoso Weather:</span></span> 
  
<span data-ttu-id="86745-208">https://weather.service.contoso.com/data.aspx?outputview=search&amp;weasearchstr=tokyo</span><span class="sxs-lookup"><span data-stu-id="86745-208">https://weather.service.contoso.com/data.aspx?outputview=search&amp;weasearchstr=tokyo</span></span>
  
<span data-ttu-id="86745-p115">Tiempo de Contoso responde con el siguiente código XML para proporcionar el código de ubicación de Tokio. El XML se ajusta a la Outlook en el esquema XML de ubicación de tiempo. Tenga en cuenta que es común para los servicios de tiempo obtener datos de más de una ubicación (por ejemplo, si la ubicación seleccionada es un área metropolitana mayor). En este ejemplo, la respuesta de Tokio incluye dos ubicaciones, cada uno entre en un elemento de [Meteorología](weather-element-weatherdata-elementoutlook-weather-location-schema.md) . Los códigos de ubicación correspondientes son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="86745-p115">Contoso Weather responds with the following XML to provide the location code for Tokyo. The XML conforms to the Outlook Weather Location XML Schema. Note that it is common for weather services to return data for more than one location (for example, if the selected location is a greater metropolitan area). In this example, the response for Tokyo includes two locations, each enclosed in a [weather](weather-element-weatherdata-elementoutlook-weather-location-schema.md) element. The corresponding location codes are as follows:</span></span> 
  
- <span data-ttu-id="86745-214">WC:JAXX0085 para el atributo **weatherlocationname** que se va a  `Tokyo, JPN`</span><span class="sxs-lookup"><span data-stu-id="86745-214">wc:JAXX0085 for the **weatherlocationname** attribute being  `Tokyo, JPN`</span></span>
    
- <span data-ttu-id="86745-215">WC:10038604 para el atributo **weatherlocationname** que se va a  `Shinjuku-ku, Tokyo, Japan`</span><span class="sxs-lookup"><span data-stu-id="86745-215">wc:10038604 for the **weatherlocationname** attribute being  `Shinjuku-ku, Tokyo, Japan`</span></span>
    
```XML
<?xml version="1.0" ?>
<weatherdata>
  <weather weatherlocationcode="wc:JAXX0085" 
    weatherlocationname="Tokyo, JPN">
  </weather>
  <weather weatherlocationcode="wc:10038604" 
    weatherlocationname="Shinjuku-ku, JPN">
  </weather>
</weatherdata>

```

### <a name="getting-weather-information-for-a-location-code"></a><span data-ttu-id="86745-216">Obtención de información meteorológica para un código de ubicación</span><span class="sxs-lookup"><span data-stu-id="86745-216">Getting weather information for a location code</span></span>

<span data-ttu-id="86745-217">Después de obtener el código de ubicación para una ubicación, Outlook anexa los parámetros descritos en el paso 3 anterior a la dirección URL base para obtener información meteorológica para ese código de ubicación.</span><span class="sxs-lookup"><span data-stu-id="86745-217">After obtaining the location code for a location, Outlook appends the parameters described in Step 3 above to the base URL to obtain weather information for that location code.</span></span>
  
<span data-ttu-id="86745-218">https://service.contoso.com/data.aspx?wealocations= _code_</span><span class="sxs-lookup"><span data-stu-id="86745-218">https://service.contoso.com/data.aspx?wealocations= _code_</span></span>
  
<span data-ttu-id="86745-219">Por ejemplo, si Outlook ha obtenido la wc:JAXX0085 de código de ubicación de la información meteorológica de Contoso de Tokio, Outlook usa este código de ubicación en la siguiente dirección URL para obtener la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="86745-219">As an example, if Outlook has obtained the location code wc:JAXX0085 from Contoso Weather for Tokyo, Outlook uses this location code in the following URL to get the weather information.</span></span>
  
https://service.contoso.com/data.aspx?wealocations=wc:JAXX0085
  
<span data-ttu-id="86745-p116">Tiempo de Contoso responde con el siguiente código XML para proporcionar información meteorológica para el código de ubicación de Tokio. El código XML se ajusta a la Outlook esquema de XML de información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="86745-p116">Contoso Weather responds with the following XML to provide the weather information for the location code for Tokyo. The XML conforms to the Outlook Weather Information XML Schema.</span></span>
  
```XML
<?xml version="1.0"?>
<weatherdata>
  <weather timezone="9" attribution="Data provided by Trey Research" 
    degreetype="F" imagerelativeurl="https://contoso.com/images/en-us/" 
    url="https://contoso.com/weather.aspx?eid=33568&amp;q=Tokyo-JPN" 
    weatherlocationname="Tokyo, JPN" 
    weatherlocationcode="wc:JAXX0085">
      <current winddisplay="9 mph NNW" windspeed="9" humidity="90" feelslike="44" 
        observationpoint="Tokyo" observationtime="06:00:00" 
        shortday="Sat" day="Saturday" date="2012-04-14" skytext="Rain" skycode="11" 
        temperature="48"/>
      <forecast shortday="Sat" day="Saturday" date="2012-04-14" precip="95" skytextday="Rain"
        skycodeday="11" high="55" low="47"/>
      <forecast shortday="Sun" day="Sunday" date="2012-04-15" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="65" low="43"/>
      <forecast shortday="Mon" day="Monday" date="2012-04-16" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="64" low="52"/>
      <forecast shortday="Tue" day="Tuesday" date="2012-04-17" precip="70" skytextday="Showers / Clear" 
        skycodeday="39" high="66" low="53"/>
      <forecast shortday="Wed" day="Wednesday" date="2012-04-18" precip="55" skytextday="Showers / Clear" 
        skycodeday="39" high="68" low="51"/>
  </weather>
</weatherdata>

```

### <a name="resetting-outlook-to-use-msn-weather"></a><span data-ttu-id="86745-222">Restablecer Outlook usar MSN meteorología</span><span class="sxs-lookup"><span data-stu-id="86745-222">Resetting Outlook to use MSN Weather</span></span>

<span data-ttu-id="86745-p117">Aunque Outlook usa MSN el tiempo de forma predeterminada, si un usuario ha personalizado la barra de meteorología para usar un servicio meteorológico diferentes y posteriormente desea volver a utilizar MSN el tiempo, el usuario simplemente puede eliminar la clave de **WeatherServiceUrl** en el registro de Windows. Eliminación de esa clave del registro, restablece Outlook para usar MSN el tiempo.</span><span class="sxs-lookup"><span data-stu-id="86745-p117">Even though Outlook uses MSN Weather by default, if a user has customized the Weather Bar to use a different weather service and subsequently wants to use MSN Weather again, the user can simply delete the **WeatherServiceUrl** key in the Windows Registry. Deleting that registry key resets Outlook to use MSN Weather.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="86745-225">Conclusión</span><span class="sxs-lookup"><span data-stu-id="86745-225">Conclusion</span></span>
<span data-ttu-id="86745-226"><a name="ol15_weatherbar_conclusion"> </a></span><span class="sxs-lookup"><span data-stu-id="86745-226"></span></span>

<span data-ttu-id="86745-p118">La barra de meteorología en el calendario de Outlook usa MSN el tiempo de forma predeterminada para proporcionar la previsión meteorológica para una ubicación especificada. Los usuarios pueden ver fácilmente información meteorológica para las ubicaciones que les interesen. Servicios de datos de tiempo de terceros también pueden integrarse con la barra de meteorología admiten la Outlook esquema XML de ubicación de tiempo y Outlook esquema de XML de información meteorológica y siguiendo un protocolo de servicio web sencillos con Outlook.</span><span class="sxs-lookup"><span data-stu-id="86745-p118">The Weather Bar in the Outlook calendar uses MSN Weather by default to provide the weather forecast for a specified location. Users can conveniently see weather information for the locations they care about. Third-party weather data services can also integrate with the Weather Bar by supporting the Outlook Weather Location XML Schema and Outlook Weather Information XML Schema and following a simple web service protocol with Outlook.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86745-230">Vea también</span><span class="sxs-lookup"><span data-stu-id="86745-230">See also</span></span>

- [<span data-ttu-id="86745-231">Outlook Weather Location XML Schema</span><span class="sxs-lookup"><span data-stu-id="86745-231">Outlook Weather Location XML Schema</span></span>](outlook-weather-location-xml-schema.md)   
- [<span data-ttu-id="86745-232">Outlook Weather Information XML Schema</span><span class="sxs-lookup"><span data-stu-id="86745-232">Outlook Weather Information XML Schema</span></span>](outlook-weather-information-xml-schema.md)
    

