---
title: Códigos de error del proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestran en la tabla siguiente.
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359860"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Códigos de error del proveedor de Outlook Social Connector

Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestran en la tabla siguiente. 
  
|**Error**|**Código de error (hexadecimal)**|**Descripción**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Error de autenticación en la red del sitio de red social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |No hay ninguna conexión disponible para conectarse al sitio de red social.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Error general de error.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Se ha producido un error interno debido a una operación no válida.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Se pasó un argumento no válido a una función.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |No se han producido cambios desde la última sincronización.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |No se encuentra un recurso.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |La solicitud al sitio de red social es válida pero no ha sido implementada por el sitio de red social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Error de memoria insuficiente.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |El proveedor OSC denegó el permiso para el recurso.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |No se admite la versión del servidor para configurar la cuenta de red social.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |El proveedor no admite esta versión de la extensibilidad del proveedor OSC.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de éxito, ADVERTENCIA y error se devuelven mediante un número de 32 bits que se denomina controlador de resultados o **HRESULT**. Un **HRESULT** no es un identificador para nada; solo es un valor de 32 bits que tiene varios campos codificados en el valor. Un resultado positivo indica que el estado es correcto, un resultado cero indica Success sin estado (S_OK) y un resultado negativo indica un error. 
  

