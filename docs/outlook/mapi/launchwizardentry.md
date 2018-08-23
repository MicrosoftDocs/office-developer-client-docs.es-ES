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
ms.openlocfilehash: f2cc9a6f97fa51a255f8c24c2bb52c912aef7718
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566253"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función que inicia la aplicación de Asistente para perfiles con el fin de agregar uno o más servicios de mensaje a un perfil. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
|Función definido implementada por:  <br/> |MAPI  <br/> |
|Llamado por una función definida:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parámetros

 _hParentWnd_
  
> [entrada] Identificador de ventana primario del autor de la llamada. Si el autor de la llamada no tiene una ventana principal, el parámetro _hParentWnd_ debe ser nulo. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcadores que indica las opciones para el Asistente para perfiles. Se pueden establecer los siguientes indicadores:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> El Asistente para perfiles es agregar sólo los servicios de mensaje que aparecen a través del parámetro _lppszServiceNameToAdd_ y no mostrar su página de selección de servicios de mensaje. 
    
MAPI_PW_FIRST_PROFILE 
  
> El perfil que se va a crear es el primero para esta estación de trabajo. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Página de perfil del Asistente para seleccionar servicios de mensajes no debe mostrarse. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> El Asistente para perfiles se inició la aplicación de configuración del Panel de Control. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Se deben mostrar cuadros de diálogo de configuración a sólo de los proveedores de servicios y las páginas del Asistente de perfiles no deben aparecer. Esta marca sólo se puede establecer si se establece la marca MAPI_PW_ADD_SERVICE_ONLY. 
    
 _lppszServiceNameToAdd_
  
> [entrada] Puntero a una matriz de cadenas que contiene los nombres de los servicios de mensaje que se agregará al perfil. La matriz debe terminar con un valor NULL. 
    
 _cbBufferMax_
  
> [entrada] Tamaño del búfer que señala el parámetro _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> [out] Puntero a un búfer de cadena donde la función basada en **LAUNCHWIZARDENTRY** devuelve el nombre del perfil creado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación. Las posibilidades incluyen error al inicializar el subsistema MAPI para el Asistente para perfiles, incapacidad para tener acceso el perfil predeterminado y un error a devolver desde el cuadro de diálogo.
    
## <a name="remarks"></a>Comentarios

La implementación de MAPI del prototipo de la función **LAUNCHWIZARDENTRY** es el punto de entrada a la aplicación del Asistente para el perfil MAPI. En este punto de entrada **LaunchWizard**nombres de MAPI. 
  
Cuando se establece la marca MAPI_PW_ADD_SERVICE_ONLY en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- El indicador MAPI_PW_LAUNCHED_BY_CONFIG desactiva la página de bienvenida que no se muestren. 
    
- Los indicadores MAPI_PW_HIDE_SERVICES_LIST y MAPI_PW_PROVIDER_UI_ONLY son útiles sólo cuando no hay ningún perfil predeterminado. En este caso, estos marcadores determinan qué perfil de Asistente para la página que se mostrará. 
    
- Si existe un perfil de forma predeterminada, ninguna de las páginas del Asistente de perfiles son que se mostrará. 
    
- Si existe un perfil predeterminado, servicio de un solo mensaje está en la lista a través del parámetro _lppszServiceNameToAdd_ , y el servicio de mensajes ya está en el perfil predeterminado, el Asistente para perfiles devuelve S_OK sin agregar nada para el perfil. 
    
Para que cada servicio de mensajes que se agregará al perfil, el Asistente para perfiles de llamadas de función de punto de entrada del servicio basada en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) . Para cada proveedor de servicios seleccionado en un servicio de mensajes que se agregará al perfil, el Asistente para perfiles llama a función de punto de entrada del proveedor según el prototipo [WIZARDENTRY](wizardentry.md) . Durante la configuración interactiva, cada evento de usuario en las páginas de propiedades hace que el Asistente para perfiles llamar a la función de devolución de llamada del proveedor según el prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Si va a agregar al perfil de un proveedor de servicios es compatible con las páginas del Asistente de perfiles, debe permitir la configuración mediante programación del perfil.
  

