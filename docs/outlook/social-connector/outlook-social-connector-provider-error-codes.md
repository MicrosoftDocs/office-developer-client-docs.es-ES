---
title: Códigos de error de proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestra en la siguiente tabla.
ms.openlocfilehash: 9e9abfda5930926a873ac37d3372eff7100be8a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821211"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Códigos de error de proveedor de Outlook Social Connector

Los proveedores deben devolver errores al autor de la llamada mediante uno de los códigos de error que se muestra en la siguiente tabla. 
  
|**Error**|**Código de error (hexadecimal)**|**Descripción**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Error de autenticación en la red del sitio de red social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |No hay ninguna conexión disponible para conectarse al sitio de red social.  <br/> |
|OSC_E_FAIL  <br/> |0 x 80004005  <br/> |Error de fallo general.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Se ha producido un error interno debido a una operación no válida.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0 x 80070057  <br/> |Se ha pasado un argumento no válido a una función.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |No ha habido cambios desde la última sincronización.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |No se encuentra un recurso.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0 x 80004001  <br/> |La solicitud para el sitio de red social es válida pero no se ha implementado por el sitio de red social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Se produjo un error de falta de memoria.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |El proveedor de OSC denegado el permiso para el recurso.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |No se admite la versión del servidor para configurar la cuenta de redes sociales.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |El proveedor no es compatible con esta versión de extensibilidad del proveedor OSC.  <br/> |
   
## <a name="remarks"></a>Notas

Correcto, advertencia y los valores de error se devuelven mediante el uso de un número de 32 bits que se llama a un controlador de resultado o **HRESULT**. Un **HRESULT** no es un identificador de nada; es simplemente un valor de 32 bits que tiene varios campos codificados en el valor. Un resultado positivo indica éxito con el estado de un resultado de cero indica éxito sin estado (S_OK) y un resultado negativo indica un error. 
  

