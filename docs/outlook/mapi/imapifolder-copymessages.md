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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817230"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _lpMsgList_
  
> [entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o mensajes para copiar o mover. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino al que apunta el parámetro _lpDestFolder_ . Si se pasa NULL da como resultado el proveedor de servicios de devolución de la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros autores de llamadas pueden establecer el parámetro _lpInterface_ para IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [entrada] Un puntero a la carpeta abierta para recibir los mensajes que se ha movido o copiados.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método. El parámetro _ulUIParam_ se omite a menos que el cliente establece el indicador MESSAGE_DIALOG en el parámetro _ulFlags_ y pasa NULL en el parámetro _lpProgress_ . 
    
 _lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Informa al proveedor de almacén de mensajes para devolver inmediatamente MAPI_E_DECLINE_COPY si implementa **IMAPIFolder::CopyMessages** mediante una llamada al método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) o [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) del objeto de la compatibilidad con. 
    
MESSAGE_DIALOG 
  
> Muestra un indicador de progreso mientras se realiza la operación.
    
MESSAGE_MOVE 
  
> El mensaje o mensajes son va a mover en lugar de copiado. Si no se establece MESSAGE_MOVE, se copian los mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje o los mensajes se hayan copiado correctamente o movido.
    
MAPI_E_DECLINE_COPY 
  
> El proveedor implementa este método mediante una llamada a un método del objeto de soporte, y el autor de la llamada ha pasado la marca MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se completó correctamente, pero no todas las entradas se han movido o copiado correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Notas

El método **IMAPIFolder::CopyMessages** copia o mueve los mensajes a otra carpeta. 
  
Los mensajes que se abren con lectura y escritura permiso puede mover o copiar. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si va a copiar los mensajes a otro almacén de mensajes sin utilizar el método [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , primero debe llamar [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) con el conjunto de marca GENERATE_RECEIPT_ONLY. El almacén de mensajes receptor no es responsable de la generación de informes de lectura para los mensajes que se ha movido o copiados. Si se llama a **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, no se llama a **SetReadFlags**; MAPI lo llamará. 
  
La implementación puede mover o copiar los mensajes en cualquier orden y generación de informes de estado de lectura en cualquier orden. Es decir, puede finalice de copiar los mensajes antes de generar cualquiera de los informes de estado de lectura o enviar los informes antes de la implementación inicia la operación de copia. Sin embargo, lea informes deben enviarse para que todos los mensajes que se copian, independientemente de si la copia es correcta.
  
Cuando la operación de copiar o mover implica más de un mensaje, realizar la operación más completo posible. No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes.
  
Intente mantener los identificadores de entrada a través de las operaciones de mover o copiar. También debe conservar los identificadores de entrada, aunque no es necesario.
  
Enviar notificaciones al mover o copiar mensajes para que los clientes se prevenido que sus llamadas a los métodos de la de los mensajes [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pueden producir un error. 
  
No se incluyen el estado de un mensaje en la copia o la operación de movimiento. Mover o copiar un estado de mensaje en gran medida afecta al rendimiento.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Use **IMAPIFolder::CopyMessages** para rellenar las carpetas de resultados de búsqueda, donde los mensajes a menudo se agrupan por carpeta primaria. 
  
Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** correctamente haya copiado o movido todos los mensajes.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** no pudo copiar o mover todos los mensajes correctamente.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** no pudo completar.  <br/> |Cualquier valor de error  <br/> |
   
Cuando **IMAPIFolder::CopyMessages** es no se puede completar, no asuma que se ha realizado ningún trabajo. Es posible que han sido **IMAPIFolder::CopyMessages** capaz de copiar o mover mensajes de uno o varios antes de encontrar el error. 
  
## <a name="see-also"></a>Ver también



[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

