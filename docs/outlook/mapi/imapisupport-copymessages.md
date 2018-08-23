---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591040"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve los mensajes de una carpeta a otra carpeta.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpSrcInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que contiene los mensajes que se pueden copiar o mover.
    
 _lpSrcFolder_
  
> [entrada] Un puntero a la carpeta que contiene los mensajes que se pueden copiar o mover.
    
 _lpMsgList_
  
> [entrada] Un puntero a una matriz de identificadores de entrada que identifican los mensajes para ser copiado o movido. 
    
 _lpDestInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino para los mensajes que se ha movido o copiados.
    
 _lpDestFolder_
  
> [entrada] Un puntero a la carpeta de destino para los mensajes que se ha movido o copiados. Esta carpeta debe estar abierta.
    
 _ulUIParam_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MESSAGE_DIALOG 
  
> Solicita la visualización de un indicador de progreso.
    
MESSAGE_MOVE 
  
> Se va a mover los mensajes, en lugar de copiado. Si no se establece MESSAGE_MOVE, se copian los mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de copiar o mover fue correcta.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::CopyMessages** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyMessages** en su implementación de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o más mensajes de una carpeta a otra. Como parte de la llamada **IMAPISupport::CopyMessages** , puede especificar el proveedor de almacén de mensajes que MAPI debe mostrar un indicador de progreso. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

