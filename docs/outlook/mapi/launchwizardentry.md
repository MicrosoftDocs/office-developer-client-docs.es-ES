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
  
Define una función que inicia la aplicación asistente para perfiles con el fin de agregar uno o más servicios de mensajes a un perfil. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
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
  
> [in] Identificador de la ventana principal del autor de la llamada. Si el autor de la llamada no tiene una ventana principal, el  _parámetro hParentWnd_ debe ser NULL. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que indican las opciones del Asistente para perfiles. Se pueden establecer las siguientes marcas:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> El Asistente para perfiles es agregar solo los servicios de mensajes enumerados a través del parámetro  _lppszServiceNameToAdd_ y no mostrar su página para seleccionar servicios de mensajes. 
    
MAPI_PW_FIRST_PROFILE 
  
> El perfil que se va a crear es el primero para esta estación de trabajo. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> No se debe mostrar la página del Asistente para perfiles para seleccionar servicios de mensajes. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> La aplicación de configuración del Panel de control ha iniciado el Asistente para perfiles. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Solo se deben mostrar los cuadros de diálogo de configuración de los proveedores de servicios y no deben aparecer las páginas del Asistente para perfiles. Esta marca solo se puede establecer si se MAPI_PW_ADD_SERVICE_ONLY marca. 
    
 _lppszServiceNameToAdd_
  
> [in] Puntero a una matriz de cadenas que contiene los nombres de los servicios de mensaje que se van a agregar al perfil. La matriz debe terminar con un valor NULL. 
    
 _cbBufferMax_
  
> [in] Tamaño del búfer al que apunta el _parámetro lpszNewProfileName._ 
    
 _lpszNewProfileName_
  
> [salida] Puntero a un búfer de cadena donde la función basada en **LAUNCHWIZARDENTRY** devuelve el nombre del perfil creado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación. Entre las posibilidades se incluyen un error al inicializar el subsistema MAPI para el Asistente para perfiles, la incapacidad para obtener acceso al perfil predeterminado y un retorno de error desde el cuadro de diálogo.
    
## <a name="remarks"></a>Comentarios

La implementación MAPI del prototipo de **función LAUNCHWIZARDENTRY** es el punto de entrada en la aplicación del Asistente para perfiles MAPI. MAPI nombra a este punto **de entrada LaunchWizard**. 
  
Cuando la MAPI_PW_ADD_SERVICE_ONLY se establece en el  _parámetro ulFlags,_ se aplican las siguientes reglas: 
  
- La MAPI_PW_LAUNCHED_BY_CONFIG impide que se muestre la página de bienvenida. 
    
- Las MAPI_PW_HIDE_SERVICES_LIST y MAPI_PW_PROVIDER_UI_ONLY son útiles solo cuando no hay ningún perfil predeterminado. En este caso, estas marcas determinan qué página del Asistente para perfiles se va a mostrar. 
    
- Si existe un perfil predeterminado, no se mostrará ninguna de las páginas del Asistente para perfiles. 
    
- Si existe un perfil predeterminado, solo aparece un servicio de mensajes a través del parámetro  _lppszServiceNameToAdd_ y ese servicio de mensajes ya está en el perfil predeterminado, el Asistente para perfiles devuelve S_OK sin agregar nada al perfil. 
    
Para cada servicio de mensajes que se agregará al perfil, el Asistente para perfiles llama a la función de punto de entrada del servicio en función del prototipo [MSGSERVICEENTRY.](msgserviceentry.md) Para que cada proveedor de servicios seleccionado de un servicio de mensajes se agregará al perfil, el Asistente para perfiles llama a la función de punto de entrada del proveedor en función del prototipo [WIZARDENTRY.](wizardentry.md) Durante la configuración interactiva, cada evento de usuario de las páginas de propiedades hace que el Asistente para perfiles llame a la función de devolución de llamada del proveedor en función del prototipo [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md) 
  
Si un proveedor de servicios que se agrega al perfil admite las páginas del Asistente para perfiles, debe permitir la configuración mediante programación del perfil.
  

