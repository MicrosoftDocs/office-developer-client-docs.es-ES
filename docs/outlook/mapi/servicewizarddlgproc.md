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
  
Define una función de devolución de llamada invocada por el Asistente para perfiles para permitir que un proveedor de servicios reaccione a eventos de usuario cuando se muestran las hojas de propiedades o páginas del proveedor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
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
  
> [in] Identificador de ventana al cuadro de diálogo Asistente para perfiles. 
    
_wMsgID_
  
> [in] Mensaje de ventana que se va a procesar. Además de los mensajes de ventana normales esperados por un cuadro de diálogo modal, se pueden recibir los siguientes mensajes:
    
WM_CLOSE 
  
> Se ha completado el Asistente para perfiles. El proveedor de servicios debe realizar toda la limpieza necesaria, como la desasignación de cualquier memoria asignada dinámicamente. 
    
WM_COMMAND 
  
> Se ha seleccionado uno de los controles  del  proveedor o se ha hecho clic en el botón Siguiente o Atrás. El valor del  _parámetro wParam_ indica cuál de estos eventos de usuario se ha producido. 
    
WM_INITDIALOG 
  
> El usuario se ha movido a otra página de propiedades, para la que se debe inicializar el cuadro de diálogo. El proveedor debe inicializar los controles que el Asistente para perfiles ha agregado al cuadro de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> El Asistente para perfiles solicita el número de páginas que el proveedor debe mostrar. El proveedor debe devolver el número de páginas en lugar de TRUE o FALSE. Por ejemplo, use la siguiente instrucción return para indicar que deben mostrarse tres páginas:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Parámetro de 32 bits asociado con mensajes de ventana. Los valores posibles dependen del mensaje especificado en el _parámetro wMsgID._ Además de los valores esperados con los mensajes de ventana normales para un cuadro de diálogo modal, se pueden recibir los siguientes valores: 
    
WIZ_NEXT 
  
> Cuando  _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el **botón** Siguiente. 
    
WIZ_PREV 
  
> Cuando  _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el **botón** Atrás. 
    
_lParam_
  
> [in] Parámetro de 32 bits asociado con mensajes de ventana. Los valores posibles dependen del mensaje especificado en el _parámetro wMsgID._ 
    
## <a name="return-value"></a>Valor devuelto

El valor devuelto por una **función basada en SERVICEWIZARDDLGPROC** depende del mensaje de ventana recibido. Tenga en cuenta en particular el valor devuelto excepcional para el WIZ_QUERYNUMPAGES mensaje. Los valores devueltos normales son: 
  
TRUE 
  
> El proveedor de servicios ha procesado el mensaje de la ventana recibida. 
    
FALSE 
  
> El proveedor de servicios no ha procesado el mensaje de la ventana recibida.
    
## <a name="remarks"></a>Comentarios

Cuando el usuario se mueve de una página de propiedades a otra, el proveedor es responsable de ocultar los controles de la página anterior y mostrar los controles de la página siguiente o anterior. Cuando el usuario  hace clic en el botón Siguiente, se llama a la función basada en **SERVICEWIZARDDLGPROC** con el mensaje WM_COMMAND y WIZ_NEXT en el _parámetro wParam._ Los pasos siguientes describen lo que ocurre entre el momento en que el usuario hace clic en **Siguiente** y la hora en que se representan las páginas de configuración del primer proveedor. 
  
1. El Asistente para perfiles oculta los controles que se encuentran en la ventana. 
    
2. El Asistente para perfiles agrega los controles ocultos del proveedor a la página. 
    
3. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC** y envía el WM_INITDIALOG, para que el proveedor pueda inicializar los controles. 
    
4. El Asistente para perfiles **llama a SERVICEWIZARDDLGPROC** y envía WIZ_QUERYNUMPAGES mensaje. El proveedor devuelve el número de páginas que se van a mostrar. 
    
5. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC** y envía el mensaje WM_COMMAND con el parámetro  _wParam_ establecido en WIZ_NEXT o WIZ_PREV. En este momento, el proveedor devuelve FALSE {error} o revela sus controles y devuelve TRUE {success}. Si el Asistente para perfiles pasa ID_NEXT, se muestra la primera página del proveedor. Si ID_PREV se pasa, se muestra la última página. 
    
6. El Asistente para perfiles llama a la función **SERVICEWIZARDDLGPROC** del proveedor y envía el mensaje WM_COMMAND con el parámetro  _wParam_ establecido en WIZ_NEXT o WIZ_PREV (según el botón en el que el usuario haga clic). El proveedor es responsable de mostrar u ocultar sus controles y escribir sus datos en el **IMAPIProp** pasado al Asistente para perfiles para pasar por su secuencia de páginas. El proveedor debe devolver TRUE si la página siguiente o anterior se mostró correctamente y FALSE si no se pudo mostrar ni la página siguiente ni la anterior. El proveedor debe tener en cuenta cuándo está saliendo de su secuencia de páginas y responder adecuadamente ocultando sus controles y escribiendo sus datos en el perfil. 
    
7. Si el usuario se encuentra fuera del intervalo de páginas del proveedor, el Asistente para perfiles elimina los controles ocultos del proveedor del cuadro de diálogo y llama al siguiente proveedor o muestra su página siguiente si era el último proveedor. 
    

