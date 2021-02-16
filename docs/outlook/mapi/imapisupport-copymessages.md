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

## <a name="parameters"></a>Parámetros

 _lpSrcInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que contiene los mensajes que se van a copiar o mover.
    
 _lpSrcFolder_
  
> [entrada] Puntero a la carpeta que contiene los mensajes que se van a copiar o mover.
    
 _lpMsgList_
  
> [entrada] Puntero a una matriz de identificadores de entrada que identifican los mensajes que se van a copiar o mover. 
    
 _lpDestInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino de los mensajes copiados o movidos.
    
 _lpDestFolder_
  
> [entrada] Puntero a la carpeta de destino para los mensajes copiados o movidos. Esta carpeta debe estar abierta.
    
 _ulUIParam_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que MESSAGE_DIALOG marca esté establecida en  _ulFlags_.
    
 _lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que MESSAGE_DIALOG marca esté establecida en  _ulFlags_.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
MESSAGE_DIALOG 
  
> Solicita la presentación de un indicador de progreso.
    
MESSAGE_MOVE 
  
> Los mensajes deben moverse, en lugar de copiarse. Si MESSAGE_MOVE no está establecido, se copian los mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de copia o movimiento se ha realizado correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CopyMessages** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport::CopyMessages** en su implementación de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o más mensajes de una carpeta a otra. Como parte de la **llamada IMAPISupport::CopyMessages,** el proveedor del almacén de mensajes puede especificar que MAPI debe mostrar un indicador de progreso. 
  
## <a name="see-also"></a>Consulte también



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

