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
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430682"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de punto de entrada del proveedor de servicios a la que llama el Asistente para perfiles para recuperar información suficiente para mostrar las hojas de propiedades de configuración del proveedor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
|Función definida implementada por:  <br/> |Proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |Asistente para perfiles MAPI  <br/> |
   
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
  
> [entrada] Identificador de instancia de la DLL del proveedor de servicios. 
    
 _lpcsResourceName_
  
> [salida] Puntero a una cadena que contiene el nombre completo del recurso de diálogo que debe mostrar el Asistente para perfiles durante la configuración. El tamaño máximo de la cadena, incluido el terminador NULL, es de 32 caracteres. 
    
 _lppDlgProc_
  
> [salida] Puntero a un procedimiento de cuadro de diálogo estándar de Windows al que llamará el Asistente para perfiles para notificar al proveedor de varios eventos. 
    
 _lpMAPIProp_
  
> [entrada] Puntero a una implementación de interfaz de propiedades que proporciona acceso a las propiedades de configuración. 
    
 _lpMapiSupportObject_
  
> [entrada] Puntero al objeto de compatibilidad mapi aplicable a esta sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se llamó correctamente a la función **WIZARDENTRY del** proveedor de servicios. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

El Asistente para perfiles llama a la función basada en **WIZARDENTRY** cuando está listo para mostrar la interfaz de usuario de configuración del proveedor de servicios. Cuando el Asistente para perfiles haya terminado de configurar todos los proveedores, escribe las propiedades de configuración en el perfil llamando a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El nombre de la función basada en **WIZARDENTRY** debe colocarse en la WIZARD_ENTRY_NAME en MAPISVC.INF. 
  
El nombre del recurso es el del recurso de cuadro de diálogo que se representará en el panel del Asistente para perfiles. El recurso que se pasa debe contener todas las páginas de un único recurso de cuadro de diálogo. Cuando el Asistente para perfiles recibe este recurso, omite el estilo del cuadro de diálogo, pero no los estilos de control, y crea todos los controles como secundarios de la página Asistente para perfiles. Inicialmente, todos los controles están ocultos. Los proveedores deben asegurarse de que las coordenadas de sus controles estén basadas en cero o en cero y que no superen un ancho máximo de 200 unidades de diálogo y un alto máximo de 150 unidades de diálogo. Los identificadores de control inferiores a 400 están reservados para el Asistente para perfiles. El Asistente para perfiles muestra el título del proveedor en negrita sobre la interfaz de usuario del proveedor. 
  
El proveedor debe conservar el puntero de la interfaz de propiedades proporcionado en el parámetro  _lpMAPIProp_ para futuras referencias. El Asistente para perfiles solo se ocupa del conjunto más básico de propiedades y el proveedor puede usar la implementación de la interfaz de propiedades para incluir propiedades adicionales. Durante la configuración, los proveedores deben agregar sus propiedades de configuración al objeto que implementa la interfaz de propiedades. Una vez configurados todos los proveedores, el Asistente para perfiles agrega estas propiedades al perfil. 
  
Para obtener más información acerca de cómo usar esta función, vea [Compatibilidad con la configuración del servicio de mensajes.](supporting-message-service-configuration.md) 
  

