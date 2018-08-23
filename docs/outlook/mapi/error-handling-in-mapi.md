---
title: Control de errores en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d98b7cf1d6c5cdc8517ea2e653115d9a7c01e3c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593301"
---
# <a name="error-handling-in-mapi"></a>Control de errores en MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve valores de éxito, error y advertencia usando un número de 32 bits conocido como resultado controlador o HRESULT. Un HRESULT realmente no es un identificador de nada; es simplemente un valor de 32 bits con varios campos codificado en el valor. Un resultado de cero indica éxito y un resultado distinto de cero indica un error.
  
MAPI en plataformas de 32 bits funciona únicamente con valores HRESULT.
  
En la siguiente ilustración muestra el formato HRESULT para plataformas de 32 bits.
  
**Formato de HRESULT**
  
![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")
  
El bit de orden superior en el HRESULT indica si el valor devuelto representa el éxito o el fracaso. Si se establece en cero, el valor indica éxito. Si se establece en 1, indica un error.
  
La R, C, N y r bits están reservados en el valor de HRESULT.
  
El campo de instalaciones en ambas versiones indica el área de responsabilidad para el error. Existen varias funciones, pero la mayoría de los errores de MAPI utilizar FACILITY_ITF para representar errores de interfaz. Las instalaciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE. Si son necesarias nuevas instalaciones, Microsoft les asigna porque deben ser únicos. En la siguiente tabla se describe los diferentes campos de instalaciones.
  
|Instalaciones|Descripción|
|:-----|:-----|
|FACILITY_NULL  <br/> |Para los códigos de estado comunes aplicables a grandes rasgos como S_OK o E_OUTOF_MEMORY; el valor es cero.  <br/> |
|FACILITY_ITF  <br/> |Para la mayoría de los códigos estado devuelta desde los métodos de interfaz; el valor está definido por la interfaz. Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devuelto desde dos interfaces diferentes pueden tener diferentes significados.  <br/> |
|FACILITY_DISPATCH  <br/> |Errores de interfaz del enlace en [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) .  <br/> |
|FACILITY_RPC  <br/> |Para los códigos de estado devueltos por llamadas a procedimiento remoto.  <br/> |
|FACILITY_STORAGE  <br/> |Para los códigos de estado devueltos desde [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) o [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) llamadas al método relacionada con el almacenamiento estructurado. Códigos de estado con los valores de código (16 bits inferiores) de los códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.  <br/> |
   
El campo de código es un número único que se asigna para representar el error o la advertencia.
  

