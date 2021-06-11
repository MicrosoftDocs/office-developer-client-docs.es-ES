---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420377"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada para procesar teclas aceleradoras en un cuadro de diálogo de libreta de direcciones de modeless. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definida implementada por:  <br/> |MAPI  <br/> |
|Función definida llamada por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Valor específico de la implementación que se usa para pasar información de interfaz de usuario a una función. En las aplicaciones que se ejecutan en Microsoft Windows, _ulUIParam_ es el identificador de ventana principal de un cuadro de diálogo y es de tipo HWND, se convierte en un **ULONG_PTR**. Un valor de cero indica que no hay ninguna ventana primaria. 
    
 _lpvmsg_
  
> [in] Puntero a un Windows mensaje.
    
## <a name="return-value"></a>Valor devuelto

Una función con el **prototipo ACCELERATEABSDI** devuelve TRUE si controla el mensaje. 
  
## <a name="remarks"></a>Comentarios

Una función basada en el prototipo **ACCELERATEABSDI** solo se usa con un cuadro de diálogo de modeless, es decir, solo si la aplicación cliente ha establecido la marca DIALOG_SDI en el miembro _ulFlags_ de la estructura [ADRPARM.](adrparm.md) 
  
Un cuadro de diálogo de modeless comparte el bucle Windows mensaje de la aplicación cliente, en lugar de tener su propio bucle. La aplicación, que controla el bucle de mensajes, no sabe qué teclas de aceleración usa el cuadro de diálogo, por lo que llama a una función basada en **ACCELERATEABSDI** para probar y actuar sobre teclas de aceleración como CTRL+P para imprimir. 
  
El bucle de mensajes de un cliente llama a la función basada en **ACCELERATEABSDI** cuando el cliente invoca un cuadro de diálogo de libreta de direcciones modeless con el método [IAddrBook::Address.](iaddrbook-address.md) Esta llamada finaliza cuando MAPI llama a una función basada en el prototipo de función [DISMISSMODELESS.](dismissmodeless.md) 
  

