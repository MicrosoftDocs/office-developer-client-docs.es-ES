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
ms.openlocfilehash: 101e74f3e35e3664dd29e59f166b2f0af6e1dcba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592041"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada para teclas de aceleración de proceso en un cuadro de diálogo de la libreta de direcciones no modal. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definido implementada por:  <br/> |MAPI  <br/> |
|Llamado por una función definida:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Un valor específico de la implementación utilizado para pasar información de interfaz de usuario a una función. En las aplicaciones que se ejecutan en Microsoft Windows, _ulUIParam_ es el identificador de ventana primario para un cuadro de diálogo y es del tipo HWND, que se convierte en un **ULONG_PTR**. Un valor de cero indica que no hay ninguna ventana primaria. 
    
 _lpvmsg_
  
> [entrada] Puntero a un mensaje de Windows.
    
## <a name="return-value"></a>Valor devuelto

Una función con el prototipo **ACCELERATEABSDI** devuelve TRUE si controla el mensaje. 
  
## <a name="remarks"></a>Comentarios

Una función según el prototipo **ACCELERATEABSDI** sólo se utiliza con un cuadro de diálogo no modal, es decir, sólo si la aplicación cliente ha establecido el indicador DIALOG_SDI en el miembro _ulFlags_ de la estructura [ADRPARM](adrparm.md) . 
  
Un cuadro de diálogo no modal comparte bucle de mensaje de Windows de la aplicación de cliente, en lugar de tener su propio bucle. La aplicación, que controla el bucle de mensajes, no sabe qué teclas de aceleración usará el cuadro de diálogo, por lo que se llama una **ACCELERATEABSDI** según función para probar y actuar de teclas de aceleración, como CTRL + P para su impresión. 
  
Llamadas de bucle de mensaje de un cliente la **ACCELERATEABSDI** en función (función) cuando el cliente invoca un cuadro de diálogo de la libreta de direcciones no modal con el método [IAddrBook::Address](iaddrbook-address.md) . Esta llamada se termina cuando MAPI llama a una función según el prototipo de función [DISMISSMODELESS](dismissmodeless.md) . 
  

