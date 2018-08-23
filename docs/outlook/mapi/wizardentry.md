---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590361"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de punto de entrada de proveedor de servicio que el Asistente para perfiles llama para recuperar suficiente información como para mostrar las hojas de propiedades de configuración del proveedor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
|Función definido implementada por:  <br/> |Proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |Asistente para el perfil MAPI  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parámetros

 _hProviderDLLInstance_
  
> [entrada] Identificador de instancia del archivo DLL del proveedor de servicio. 
    
 _lpcsResourceName_
  
> [out] Puntero a una cadena que contiene el nombre completo del recurso de cuadro de diálogo que debe mostrar el Asistente para perfiles durante la configuración. El tamaño máximo de la cadena, incluido el terminador NULL, es de 32 caracteres. 
    
 _lppDlgProc_
  
> [out] Puntero a un procedimiento de cuadros de diálogo de Windows estándar que se llamará por el Asistente para perfiles para notificar el proveedor de varios eventos. 
    
 _lpMAPIProp_
  
> [entrada] Puntero a una implementación de la interfaz de propiedad que proporciona acceso a las propiedades de configuración. 
    
 _lpMapiSupportObject_
  
> [entrada] Puntero al objeto de compatibilidad con MAPI aplicable a esta sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Función **WIZARDENTRY** del proveedor de servicio se ha llamado correctamente. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación.
    
## <a name="remarks"></a>Comentarios

El Asistente para perfiles llama a la función **WIZARDENTRY** en función cuando está listo para mostrar la interfaz de usuario de configuración del proveedor de servicios. Cuando el Asistente para perfiles haya terminado de configurar todos los proveedores, escribe las propiedades de configuración para el perfil mediante una llamada a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

El nombre de la función **WIZARDENTRY** según se debe colocar en la entrada WIZARD_ENTRY_NAME en MAPISVC.INF. 
  
El nombre del recurso es que del recurso de diálogo que se representará en el panel del Asistente de perfil. El recurso que se pasa hacia atrás debe contener todas las páginas de un recurso de cuadro de diálogo único. Cuando el Asistente para perfiles recibe este recurso, pasa por alto el estilo del cuadro de diálogo, pero no los estilos de control y todos los controles se crea como elementos secundarios de la página del Asistente de perfil. Todos los controles inicialmente están ocultos. Deben realizar los proveedores de asegurarse de que las coordenadas de sus controles sean cero o basado en cero, y que no superen un ancho máximo de 200 unidades de cuadro de diálogo y una altura máxima de 150 unidades de cuadro de diálogo. Identificadores de control debajo de 400 están reservados para el Asistente para perfiles. El Asistente para perfiles muestra el título del proveedor en texto en negrita por encima de la interfaz de usuario del proveedor. 
  
El puntero de interfaz de propiedad proporcionado en el parámetro _lpMAPIProp_ se debe conservar por el proveedor para futuras referencias. El Asistente para perfiles se ocupa sólo el conjunto más básico de propiedades y el proveedor puede utilizar la implementación de la interfaz de la propiedad para incluir propiedades adicionales. Durante la configuración, los proveedores deben agregar sus propiedades de configuración para el objeto que implementa la interfaz (propiedad). Después de que se han configurado todos los proveedores, el Asistente para perfiles agrega estas propiedades para el perfil. 
  
Para obtener más información acerca de cómo usar esta función, vea [Compatibilidad con configuración del servicio de mensajes](supporting-message-service-configuration.md). 
  

