---
title: Outlook Códigos de error del proveedor de Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestran en la tabla siguiente.
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425354"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook Códigos de error del proveedor de Social Connector

Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestran en la tabla siguiente. 
  
|**Error**|**Código de error (hexadecimal)**|**Descripción**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Error de autenticación en la red del sitio de red social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |No hay conexión disponible para conectarse al sitio de red social.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Error general.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Se produjo un error interno debido a una operación no válida.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Se pasó un argumento no válido a una función.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |No se han producido cambios desde la última sincronización.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |No se puede encontrar un recurso.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |La solicitud al sitio de red social es válida, pero no ha sido implementada por el sitio de red social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Error de memoria insuficiente.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |El proveedor de OSC ha denegado el permiso para el recurso.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |No se admite la versión del servidor para configurar la cuenta de red social.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |El proveedor no admite esta versión de extensibilidad del proveedor de OSC.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores correctos, de advertencia y de error se devuelven mediante un número de 32 bits denominado controlador de resultados o **HRESULT**. Un **HRESULT** no es un controlador para nada; es simplemente un valor de 32 bits que tiene varios campos codificados en el valor. Un resultado positivo indica el éxito con el estado, un resultado cero indica el éxito sin estado (S_OK) y un resultado negativo indica un error. 
  

