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
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405159"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve mensajes de una carpeta a otra.
  
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta que contiene los mensajes que se van a copiar o mover.
    
 _lpSrcFolder_
  
> a Un puntero a la carpeta que contiene los mensajes que se van a copiar o mover.
    
 _lpMsgList_
  
> a Puntero a una matriz de identificadores de entrada que identifican los mensajes que se van a copiar o mover. 
    
 _lpDestInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta de destino para los mensajes copiados o movidos.
    
 _lpDestFolder_
  
> a Un puntero a la carpeta de destino para los mensajes copiados o movidos. Esta carpeta debe estar abierta.
    
 _ulUIParam_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MESSAGE_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
MESSAGE_MOVE 
  
> Los mensajes se deben mover, en lugar de copiarse. Si no se establece MESSAGE_MOVE, se copian los mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de copia o movimiento se realizó correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: CopyMessages** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport:: CopyMessages** en su implementación de [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o más mensajes de una carpeta a otra. Como parte de la llamada a **IMAPISupport:: CopyMessages** , el proveedor de almacenamiento de mensajes puede especificar que MAPI debe mostrar un indicador de progreso. 
  
## <a name="see-also"></a>Ver también



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

