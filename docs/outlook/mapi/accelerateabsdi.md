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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322130"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada para procesar teclas de aceleración en un cuadro de diálogo de la libreta de direcciones sin modo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
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
  
> a Valor específico de la implementación que se usa para pasar información de la interfaz de usuario a una función. En las aplicaciones que se ejecutan en Microsoft Windows, _ulUIParam_ es el controlador de la ventana principal de un cuadro de diálogo y es del tipo HWND, convertido a **ULONG_PTR**. Un valor de cero indica que no hay ventana principal. 
    
 _lpvmsg_
  
> a Puntero a un mensaje de Windows.
    
## <a name="return-value"></a>Valor devuelto

Una función con el prototipo **ACCELERATEABSDI** devuelve true si controla el mensaje. 
  
## <a name="remarks"></a>Comentarios

Una función basada en el prototipo **ACCELERATEABSDI** se usa solo con un cuadro de diálogo no modal, es decir, solo si la aplicación cliente ha establecido la marca DIALOG_SDI en el miembro _ulFlags_ de la estructura [ADRPARM](adrparm.md) . 
  
Un cuadro de diálogo no modal comparte el bucle de mensajes de Windows de la aplicación cliente, en lugar de tener su propio bucle. La aplicación, que controla el bucle de mensajes, no sabe qué teclas de aceleración utiliza el cuadro de diálogo, por lo que llama a una función basada en **ACCELERATEABSDI** para probar y actuar sobre teclas de aceleración, como Ctrl + P para imprimir. 
  
El bucle de mensajes de un cliente llama a la función basada en **ACCELERATEABSDI** cuando el cliente invoca un cuadro de diálogo de la libreta de direcciones sin modo con el método [IAddrBook:: Address](iaddrbook-address.md) . Esta llamada finaliza cuando MAPI llama a una función basada en el prototipo de función [DISMISSMODELESS](dismissmodeless.md) . 
  

