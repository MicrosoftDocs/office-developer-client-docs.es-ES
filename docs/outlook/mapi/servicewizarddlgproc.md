---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432383"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada invocada por el Asistente para perfiles para permitir a un proveedor de servicios reaccionar a los eventos de usuario cuando se muestran las páginas o las hojas de propiedades del proveedor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz. h  <br/> |
|Función definida implementada por:  <br/> |Proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |Asistente para perfiles MAPI  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parameters

_hDlg_
  
> a Identificador de ventana para el cuadro de diálogo Asistente para perfiles. 
    
_wMsgID_
  
> a Mensaje de ventana que se va a procesar. Además de los mensajes de ventana normales que espera un cuadro de diálogo modal, se pueden recibir los siguientes mensajes:
    
WM_CLOSE 
  
> El Asistente de perfil se ha completado. El proveedor de servicios debe realizar todas las tareas de limpieza necesarias, como cancelar la asignación de memoria asignada dinámicamente. 
    
WM_COMMAND 
  
> Se ha seleccionado uno de los controles del proveedor o se ha hace clic en el botón **siguiente** o **atrás** . El valor del parámetro _wParam_ indica cuál de estos eventos de usuario se ha producido. 
    
WM_INITDIALOG 
  
> El usuario se ha movido a otra página de propiedades, para la que debe inicializarse el cuadro de diálogo. El proveedor debe inicializar los controles que el Asistente para perfiles haya agregado al cuadro de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> El Asistente para perfiles solicita el número de páginas que el proveedor tiene que mostrar. El proveedor debe devolver el número de páginas en lugar de verdadero o falso. Por ejemplo, use la siguiente instrucción return para indicar que deben mostrarse tres páginas:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> a Un parámetro de 32 bits asociado con los mensajes de ventana. Los valores posibles dependen del mensaje especificado en el parámetro _wMsgID_ . Además de los valores que se esperan con los mensajes de ventana normales para un cuadro de diálogo modal, se pueden recibir los siguientes valores: 
    
WIZ_NEXT 
  
> Cuando _wMsgID_ contiene WM_COMMAND, el usuario hizo clic en el botón **siguiente** . 
    
WIZ_PREV 
  
> Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha realizado clic en el botón **atrás** . 
    
_lParam_
  
> a Un parámetro de 32 bits asociado con los mensajes de ventana. Los valores posibles dependen del mensaje especificado en el parámetro _wMsgID_ . 
    
## <a name="return-value"></a>Valor devuelto

El valor devuelto por una función basada en **SERVICEWIZARDDLGPROC** depende del mensaje de ventana recibido. Tenga en cuenta en concreto el valor devuelto excepcional para el mensaje WIZ_QUERYNUMPAGES. Los valores normales devueltos son: 
  
TRUE 
  
> El proveedor de servicios ha procesado el mensaje de ventana recibido. 
    
FALSE 
  
> El proveedor de servicios no ha procesado el mensaje de ventana recibido.
    
## <a name="remarks"></a>Comentarios

Cuando el usuario se mueve de una página de propiedades a otra, el proveedor es responsable de ocultar los controles de la página antigua y de mostrar los controles de la página siguiente o anterior. Cuando el usuario hace clic en el botón **siguiente** , se llama a la función basada en **SERVICEWIZARDDLGPROC** con el mensaje WM_COMMAND y WIZ_NEXT en el parámetro _wParam_ . Los pasos siguientes describen lo que ocurre entre el momento en que el usuario hace clic en **siguiente** y la hora en que se representan las páginas de configuración del primer proveedor. 
  
1. El Asistente para perfiles oculta los controles que se encuentran en la ventana. 
    
2. El Asistente para perfiles agrega los controles ocultos del proveedor a la página. 
    
3. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WM_INITDIALOG, para que el proveedor pueda inicializar los controles. 
    
4. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WIZ_QUERYNUMPAGES. El proveedor devuelve el número de páginas que se van a mostrar. 
    
5. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV. En este punto, el proveedor devuelve FALSE {error} o revela sus controles y devuelve TRUE {Success}. Si el Asistente para perfiles pasa en ID_NEXT, se muestra la primera página del proveedor. Si se pasa ID_PREV, se muestra la última página. 
    
6. El Asistente para perfiles llama a la función **SERVICEWIZARDDLGPROC** del proveedor, enviando el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV (según el botón en el que el usuario hizo clic). El proveedor es responsable de mostrar u ocultar sus controles y escribir sus datos en el **IMAPIProp** que se pasa al Asistente para perfiles para recorrer su secuencia de páginas. El proveedor debe devolver TRUE si se ha mostrado correctamente la página siguiente o anterior, y FALSE si no se puede mostrar la página siguiente ni la anterior. El proveedor debe estar al tanto de la versión fuera de su secuencia de páginas y responder de manera adecuada ocultando sus controles y escribiendo sus datos en el perfil. 
    
7. Si los pasos del usuario se encuentran fuera del intervalo de páginas del proveedor, el Asistente para perfiles elimina los controles ocultos del proveedor del cuadro de diálogo y llama al siguiente proveedor o muestra la página siguiente si ese era el último proveedor. 
    

