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
ms.openlocfilehash: fdd5d01b96c9ea756ee64f113ccb5119a9693668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594470"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada invocada por el Asistente para perfiles para permitir que un proveedor de servicios reaccionar a los eventos de usuario cuando se va a mostrar páginas o las hojas de propiedades del proveedor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiwz.h  <br/> |
|Función definido implementada por:  <br/> |Proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |Asistente para el perfil MAPI  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

_hDlg_
  
> [entrada] Identificador de ventana para el cuadro de diálogo Asistente para el perfil. 
    
_wMsgID_
  
> [entrada] El mensaje de ventana que va a procesar. Además de los mensajes de ventana regular esperados por un cuadro de diálogo modal, se pueden recibir los mensajes siguientes:
    
WM_CLOSE 
  
> Ha completado el Asistente para perfiles. El proveedor de servicios debe hacer todos los limpieza necesaria, como cancelar la asignación de alguna dinámicamente asignados a la memoria. 
    
WM_COMMAND 
  
> Se ha seleccionado uno de los controles del proveedor, o ha hecho clic en el botón **siguiente** o **Atrás** . El valor en el parámetro _wParam_ indica cuál de estos eventos de usuario se ha producido. 
    
WM_INITDIALOG 
  
> El usuario ha movido a otra página de propiedades, para el que se debe inicializar el cuadro de diálogo. El proveedor debe inicializar los controles que ha agregado el Asistente para perfiles en el cuadro de diálogo. 
    
WIZ_QUERYNUMPAGES 
  
> El número de páginas que se debe mostrar el proveedor que solicita el Asistente para perfiles. El proveedor debe devolver el número de páginas en lugar de TRUE o FALSE. Por ejemplo, use la siguiente instrucción return para indicar que deben tres páginas para que se muestre:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [entrada] Un parámetro de 32 bits asociado con los mensajes de ventana. El mensaje especificado en el parámetro _wMsgID_ dependen de los valores posibles. Además de los valores esperados con los mensajes de ventana normal para un cuadro de diálogo modal, se pueden recibir los siguientes valores: 
    
WIZ_NEXT 
  
> Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el botón **siguiente** . 
    
WIZ_PREV 
  
> Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el botón **Atrás** . 
    
_lParam_
  
> [entrada] Un parámetro de 32 bits asociado con los mensajes de ventana. El mensaje especificado en el parámetro _wMsgID_ dependen de los valores posibles. 
    
## <a name="return-value"></a>Valor devuelto

El valor devuelto por una función de **SERVICEWIZARDDLGPROC** en función depende en el mensaje de ventana recibido. Tenga en cuenta que las excepcionales devuelven el valor para el mensaje WIZ_QUERYNUMPAGES. Los valores devueltos normales son: 
  
TRUE 
  
> El proveedor de servicios ha procesado el mensaje de ventana recibidos. 
    
FALSE 
  
> El proveedor de servicios no procesó el mensaje de ventana recibidos.
    
## <a name="remarks"></a>Comentarios

Cuando el usuario se mueve de una página de propiedades a otra, el proveedor es responsable de la ocultación de controles de la página anterior y que muestra los controles de la página siguiente o anterior. Cuando el usuario hace clic en el botón **siguiente** , se llama a la función **SERVICEWIZARDDLGPROC** en función con el mensaje WM_COMMAND y WIZ_NEXT en el parámetro _wParam_ . Los pasos siguientes describen lo que se produce entre el momento en que el usuario hace clic en **siguiente** y la hora en que se presentan las páginas de configuración del proveedor en la primera. 
  
1. El Asistente para perfiles oculta todos los controles que se encuentran en la ventana. 
    
2. El Asistente para perfiles agrega los controles ocultos del proveedor a la página. 
    
3. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviar el mensaje WM_INITDIALOG, por lo que el proveedor puede inicializar los controles. 
    
4. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, envía el mensaje WIZ_QUERYNUMPAGES. El proveedor devuelve el número de páginas que se muestran. 
    
5. El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviar el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV. En este momento, el proveedor ya sea devuelve FALSE {error} o revela sus controles y devuelve TRUE {éxito}. Si el Asistente para perfiles pasa ID_NEXT, se muestra la primera página del proveedor. Si se pasa ID_PREV, se muestra la última página. 
    
6. El Asistente para perfiles llama (función) **SERVICEWIZARDDLGPROC** del proveedor, enviar el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV (dependiendo de qué botón hizo clic el usuario). El proveedor es responsable de mostrar u ocultar sus controles y escribir sus datos en el **IMAPIProp** se pasa al asistente paso a paso a través de su secuencia de páginas de perfil. El proveedor debe devolver TRUE si la página siguiente o anterior se mostró correctamente, y FALSE si ni la página siguiente ni anterior se pudieron mostrar. El proveedor debe tener en cuenta cuando está pasando fuera de su secuencia de páginas y responder de forma adecuada ocultando sus controles y escribir sus datos en el perfil. 
    
7. Si el usuario pasos fuera de intervalo del proveedor de páginas, el Asistente para perfiles elimina los controles ocultos del proveedor desde el cuadro de diálogo y llama al proveedor de siguiente o muestra su página siguiente si era el último proveedor. 
    

