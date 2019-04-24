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
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287286"
---
# <a name="error-handling-in-mapi"></a>Control de errores en MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los valores de éxito, ADVERTENCIA y error se devuelven usando un número de 32 bits conocido como controlador de resultado o HRESULT. Un HRESULT realmente no es un identificador para nada; solo es un valor de 32 bits con varios campos codificados en el valor. Un resultado cero indica que se ha realizado correctamente y un resultado distinto de cero indica un error.
  
Las plataformas MAPI en 32 bits funcionan únicamente con valores HRESULT.
  
En la siguiente ilustración se muestra el formato HRESULT para las plataformas de 32 bits.
  
**Formato de HRESULT**
  
![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")
  
El bit de orden superior del HRESULT indica si el valor devuelto representa el éxito o el error. Si se establece en cero, el valor indica que se ha realizado correctamente. Si se establece en 1, indica un error.
  
Los bits R, C, N y r están reservados en el HRESULT.
  
El campo Facility de ambas versiones indica el área de responsabilidad del error. Hay varias instalaciones, pero la gran mayoría de los errores de MAPI usan FACILITY_ITF para representar errores de interfaz. Las funciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE. Si se necesitan nuevas instalaciones, Microsoft les asignará los usuarios, ya que deben ser únicas. En la tabla siguiente se describen los distintos campos de instalaciones.
  
|Facility|Descripción|
|:-----|:-----|
|FACILITY_NULL  <br/> |Para los códigos de estado comunes de gran aplicación, como S_OK o E_OUTOF_MEMORY; el valor es cero.  <br/> |
|FACILITY_ITF  <br/> |Para la mayoría de los códigos de estado devueltos desde los métodos de interfaz; la interfaz define el valor. Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devueltos por dos interfaces diferentes pueden tener diferentes significados.  <br/> |
|FACILITY_DISPATCH  <br/> |Para los errores de la interfaz [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) de enlace en tiempo de ejecución.  <br/> |
|FACILITY_RPC  <br/> |Para los códigos de estado devueltos de las llamadas a procedimientos remotos.  <br/> |
|FACILITY_STORAGE  <br/> |Para los códigos de estado devueltos desde las llamadas al método [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) o [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas con el almacenamiento estructurado. Los valores de códigos de estado con código (16 bits inferiores) en el intervalo de códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.  <br/> |
   
El campo Código es un número único que se asigna para representar el error o la advertencia.
  

