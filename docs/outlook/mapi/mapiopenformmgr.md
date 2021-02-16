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
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418053"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una [interfaz IMAPIFormMgr](imapiformmgriunknown.md) en un objeto proveedor de bibliotecas de formularios en el contexto de una sesión existente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
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
  
> [salida] Puntero a la interfaz **IMAPIFormMgr devuelta.** 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Después de que una aplicación cliente realiza una llamada a la función **MAPIOpenFormMgr,** la mayoría de las interacciones relacionadas con formularios posteriores tienen lugar a través del proveedor de bibliotecas de formularios o una interfaz devuelta por el proveedor de bibliotecas de formularios. La **interfaz IMAPIFormMgr permite** al cliente trabajar con controladores de mensajes y realizar resoluciones entre clases de mensajes y bibliotecas de formularios. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp abre el administrador de formularios para que se pueda seleccionar un formulario.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI usa el **método MAPIOpenFormMgr** para abrir el administrador de formularios de modo que se pueda seleccionar un formulario.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

