---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437388"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función que inicia la aplicación del Asistente para perfiles con el fin de agregar uno o más servicios de mensajes a un perfil. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz. h  <br/> |
|Función definida implementada por:  <br/> |MAPI  <br/> |
|Función definida llamada por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parameters

 _hParentWnd_
  
> a Identificador de la ventana primaria del autor de la llamada. Si el autor de la llamada no tiene una ventana primaria, el parámetro _hParentWnd_ debe ser nulo. 
    
 _ulFlags_
  
> a Máscara de máscara de los indicadores que indican opciones para el Asistente para perfiles. Se pueden establecer los siguientes indicadores:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> El Asistente para perfiles es agregar únicamente los servicios de mensajes enumerados mediante el parámetro _lppszServiceNameToAdd_ y no mostrar su página para seleccionar los servicios de mensajes. 
    
MAPI_PW_FIRST_PROFILE 
  
> El perfil que se creará es el primero de esta estación de trabajo. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> No debe mostrarse la página del Asistente para perfiles para la selección de servicios de mensajes. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> El Asistente para perfiles fue iniciado por la aplicación de configuración del panel de control. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Solo se mostrarán los cuadros de diálogo Configuración de los proveedores de servicios y las páginas del Asistente para perfiles no deben aparecer. Esta marca solo se puede establecer si está establecida la marca MAPI_PW_ADD_SERVICE_ONLY. 
    
 _lppszServiceNameToAdd_
  
> a Puntero a una matriz de cadenas que contiene los nombres de los servicios de mensaje que se van a agregar al perfil. La matriz debe terminar con un valor NULL. 
    
 _cbBufferMax_
  
> a Tamaño del búfer al que señala el parámetro _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> contempla Puntero a un búfer de cadena donde la función basada en **LAUNCHWIZARDENTRY** devuelve el nombre del perfil creado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación. Entre las posibilidades se incluye el error al inicializar el subsistema MAPI para el Asistente para perfiles, la incapacidad para obtener acceso al perfil predeterminado y un error de devolución del cuadro de diálogo.
    
## <a name="remarks"></a>Comentarios

La implementación de MAPI del prototipo de función **LAUNCHWIZARDENTRY** es el punto de entrada a la aplicación Asistente para perfiles MAPI. MAPI denomina este punto de entrada **LaunchWizard**. 
  
Cuando se establece la marca MAPI_PW_ADD_SERVICE_ONLY en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- La marca MAPI_PW_LAUNCHED_BY_CONFIG impide que se muestre la página de bienvenida. 
    
- Los indicadores MAPI_PW_HIDE_SERVICES_LIST y MAPI_PW_PROVIDER_UI_ONLY solo son útiles cuando no hay un perfil predeterminado. En este caso, estos indicadores determinan qué página del asistente de perfil se va a mostrar. 
    
- Si existe un perfil predeterminado, no se mostrará ninguna de las páginas del Asistente para perfiles. 
    
- Si existe un perfil predeterminado, solo se muestra un servicio de mensajes a través del parámetro _lppszServiceNameToAdd_ y ese servicio de mensajes ya se encuentra en el perfil predeterminado, el Asistente para perfiles Devuelve S_OK sin agregar nada al perfil. 
    
Por cada servicio de mensajes que se va a agregar al perfil, el Asistente de perfiles llama a la función de punto de entrada del servicio en función del prototipo [MSGSERVICEENTRY](msgserviceentry.md) . Para cada proveedor de servicios seleccionado de un servicio de mensajes que se va a agregar al perfil, el Asistente de perfiles llama a la función de punto de entrada del proveedor en función del prototipo [WIZARDENTRY](wizardentry.md) . Durante la configuración interactiva, todos los eventos de usuario en las páginas de propiedades hacen que el Asistente para perfiles llame a la función de devolución de llamada del proveedor en función del prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Si un proveedor de servicios que se va a agregar al perfil admite las páginas del Asistente para perfiles, debe permitir la configuración mediante programación del perfil.
  

