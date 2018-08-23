---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586035"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre una interfaz [IMAPIFormMgr](imapiformmgriunknown.md) en un objeto de proveedor de la biblioteca de formulario en el contexto de una sesión existente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Parámetros

 _pSession_
  
> [entrada] Puntero a la sesión en uso por la aplicación cliente.
    
 _ppmgr_
  
> [out] Puntero a la interfaz devuelta de **IMAPIFormMgr** . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Después de que una aplicación cliente realiza una llamada a la función **MAPIOpenFormMgr** , la mayoría relacionadas con formularios de las interacciones subsiguientes tienen lugar a través de una interfaz devuelto por el proveedor de la biblioteca de formulario o el proveedor de la biblioteca de formulario. La interfaz de **IMAPIFormMgr** permite que el cliente trabajar con controladores de mensajes y realizar resoluciones entre las clases de mensajes y las bibliotecas de formularios. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp abre el Administrador de formularios de modo que se puede seleccionar un formulario.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI usa el método **MAPIOpenFormMgr** para abrir el Administrador de formulario, por lo que se puede seleccionar un formulario.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

