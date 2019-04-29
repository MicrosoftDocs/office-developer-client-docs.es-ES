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
  
Copia o mueve uno o más mensajes.
  
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
  
> a Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que se van a copiar o mover. 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta de destino a la que apunta el parámetro _lpDestFolder_ . Pasar resultados NULL, el proveedor de servicios devuelve la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros llamadores pueden establecer el parámetro _lpInterface_ en IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> a Un puntero a la carpeta abierta para recibir los mensajes copiados o movidos.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra. El parámetro _ulUIParam_ se omite a menos que el cliente establezca la marca MESSAGE_DIALOG en el parámetro _ULFLAGS_ y pase null en el parámetro _lpProgress_ . 
    
 _lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Informa al proveedor del almacén de mensajes para que devuelva inmediatamente MAPI_E_DECLINE_COPY si implementa **IMAPIFolder:: CopyMessages** al llamar al método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) o [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) del objeto support. 
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso mientras se lleva a cabo la operación.
    
MESSAGE_MOVE 
  
> El mensaje o los mensajes se moverán en lugar de copiarse. Si no se establece MESSAGE_MOVE, se copian los mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje o los mensajes se han copiado o movido correctamente.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método llamando a un método de objeto de soporte y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero no todas las entradas se han copiado o movido correctamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: CopyMessages** copia o mueve mensajes a otra carpeta. 
  
Los mensajes que se abren con el permiso de lectura y escritura se pueden mover o copiar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si va a copiar mensajes a otro almacén de mensajes sin usar el método [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) , primero debe llamar a [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) con la marca GENERATE_RECEIPT_ONLY establecida. El almacén de mensajes receptor no es responsable de generar informes de lectura para los mensajes copiados o movidos. Si está llamando a **IMAPISupport:: CopyMessages** para implementar **IMAPIFolder:: CopyMessages**, no llame a **SetReadFlags**; MAPI lo llamará. 
  
La implementación puede mover o copiar los mensajes en cualquier orden y generar informes de estado de lectura en cualquier orden. Es decir, puede terminar de copiar los mensajes antes de generar cualquiera de los informes de estado de lectura o enviar los informes antes de que la implementación inicie la operación de copia. Sin embargo, se deben enviar informes de lectura para que se copien todos los mensajes, independientemente de si la copia se ha realizado correctamente.
  
Cuando la operación de copia o movimiento implica más de un mensaje, realice la operación lo más completamente posible. No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes.
  
Intente mantener los identificadores de entrada en las operaciones de movimiento o copia. También debe conservar los identificadores de entrada, aunque no es necesario.
  
Enviar notificaciones cuando se mueven o se copian mensajes para que los clientes se vean prevenido de que las llamadas a los métodos ' [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de los mensajes podrían producir un error. 
  
No incluya el estado de un mensaje en la operación de copiar o mover. Mover o copiar el estado de un mensaje afecta en gran medida al rendimiento.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Use **IMAPIFolder:: CopyMessages** para rellenar las carpetas de resultados de búsqueda, donde los mensajes se suelen agrupar por carpeta principal. 
  
Espere estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**IMAPIFolder:: CopyMessages** ha copiado o movido correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**IMAPIFolder:: CopyMessages** no pudo copiar o mover correctamente todos los mensajes.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder:: CopyMessages** no se pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando **IMAPIFolder:: CopyMessages** no se puede completar, no dé por supuesto que no se ha realizado ningún trabajo. **IMAPIFolder:: CopyMessages** podría haber podido copiar o mover uno o más mensajes antes de que se procontrase el error. 
  
## <a name="see-also"></a>Ver también



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

