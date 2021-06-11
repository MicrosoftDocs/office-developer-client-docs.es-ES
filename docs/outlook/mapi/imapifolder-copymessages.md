---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424458"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve uno o varios mensajes.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> [in] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que se copian o se mueven. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino a la que apunta el _parámetro lpDestFolder._ Si se pasa NULL, el proveedor de servicios devuelve la interfaz de carpeta estándar, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros autores de llamadas pueden establecer el parámetro lpInterface en  _IID_IUnknown,_ IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Puntero a la carpeta abierta para recibir los mensajes copiados o movidos.
    
 _ulUIParam_
  
> [in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método. El _parámetro ulUIParam_ se omite a menos que el cliente establece la marca MESSAGE_DIALOG en el parámetro _ulFlags_ y pasa NULL en el parámetro _lpProgress._ 
    
 _lpProgress_
  
> [in] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI. El  _parámetro lpProgress_ se omite a menos que la marca MESSAGE_DIALOG esté establecida en  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se realiza la operación de copiar o mover. Se pueden establecer las siguientes marcas:
    
MAPI_DECLINE_OK 
  
> Informa al proveedor del almacén de mensajes para que devuelva inmediatamente MAPI_E_DECLINE_COPY si implementa **IMAPIFolder::CopyMessages** llamando al método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) o [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) del objeto de soporte técnico. 
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso a medida que avanza la operación.
    
MESSAGE_MOVE 
  
> El mensaje o los mensajes se deben mover en lugar de copiarse. Si MESSAGE_MOVE no está establecido, los mensajes se copian.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje o los mensajes se han copiado o movido correctamente.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método llamando a un método de objeto de soporte técnico y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todas las entradas se han copiado o movido correctamente. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::CopyMessages** copia o mueve mensajes a otra carpeta. 
  
Los mensajes que se abren con permiso de lectura y escritura se pueden mover o copiar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si va a copiar mensajes en otro almacén de mensajes sin usar el método [IMAPISupport::CopyMessages,](imapisupport-copymessages.md) primero debe llamar a [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) con el conjunto de marcas GENERATE_RECEIPT_ONLY. El almacén de mensajes de recepción no es responsable de generar informes de lectura para los mensajes copiados o movidos. Si llama a **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, no llame a **SetReadFlags**; MAPI lo llamará. 
  
La implementación puede mover o copiar los mensajes en cualquier orden y generar informes de estado de lectura en cualquier orden. Es decir, puede terminar de copiar mensajes antes de generar cualquiera de los informes de estado de lectura o enviar los informes antes de que la implementación inicie la operación de copia. Sin embargo, se deben enviar informes de lectura para que todos los mensajes se copien, independientemente de si la copia se ha realizado correctamente.
  
Cuando la operación de copiar o mover implica más de un mensaje, realice la operación lo más completa posible. No detenga la operación prematuramente a menos que se produzca un error que esté fuera de su control, como que se esté quedando sin memoria, que se esté quedando sin espacio en disco o que se produzcan daños en el almacén de mensajes.
  
Intente mantener los identificadores de entrada en las operaciones de movimiento o copia. También debe conservar los identificadores de entrada, aunque no es necesario.
  
Envíe notificaciones al mover o copiar mensajes para que los clientes se den por anticipado que sus llamadas a los métodos [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de los mensajes pueden producir un error. 
  
No incluya el estado de un mensaje en la operación de copiar o mover. Mover o copiar un estado de mensaje afecta en gran medida al rendimiento.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Use **IMAPIFolder::CopyMessages** para rellenar carpetas de resultados de búsqueda, donde los mensajes suelen agruparse por carpeta principal. 
  
Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** ha copiado o movido correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** no pudo copiar o mover correctamente todos los mensajes.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando **IMAPIFolder::CopyMessages** no se pueda completar, no suponga que no se ha realizado ningún trabajo. **IMAPIFolder::CopyMessages** podría haber podido copiar o mover uno o más mensajes antes de encontrar el error. 
  
## <a name="see-also"></a>Vea también



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

