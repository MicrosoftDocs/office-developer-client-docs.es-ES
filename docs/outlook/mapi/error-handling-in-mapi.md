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
  
Los valores correctos, de advertencia y de error se devuelven con un número de 32 bits conocido como identificador de resultados o HRESULT. Un HRESULT no es realmente un controlador para nada; es simplemente un valor de 32 bits con varios campos codificados en el valor. Un resultado cero indica éxito y un resultado distinto de cero indica un error.
  
MAPI en plataformas de 32 bits funciona únicamente con valores HRESULT.
  
En la siguiente ilustración se muestra el formato HRESULT para plataformas de 32 bits.
  
**Formato de HRESULT**
  
![Formato HRESULT con](media/amapi_49.gif "formato HRESULT")
  
El bit de orden alto en el HRESULT indica si el valor devuelto representa éxito o error. Si se establece en cero, el valor indica que se ha hecho correctamente. Si se establece en 1, indica un error.
  
Los bits R, C, N y r están reservados en el HRESULT.
  
El campo de la instalación en ambas versiones indica el área de responsabilidad del error. Existen varias funciones, pero la mayoría de los errores MAPI usan FACILITY_ITF para representar errores de interfaz. Las instalaciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE. Si son necesarias nuevas instalaciones, Microsoft las asigna porque deben ser únicas. En la tabla siguiente se describen los distintos campos de la instalación.
  
|Facility|Description|
|:-----|:-----|
|FACILITY_NULL  <br/> |Para códigos de estado comunes ampliamente aplicables, como S_OK o E_OUTOF_MEMORY; el valor es cero.  <br/> |
|FACILITY_ITF  <br/> |Para la mayoría de los códigos de estado devueltos de los métodos de interfaz; el valor se define mediante la interfaz. Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devuelto desde dos interfaces diferentes pueden tener significados diferentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Para errores de interfaz [IDispatch de enlace en](https://msdn.microsoft.com/library/ms221608.aspx) tiempo de ejecución.  <br/> |
|FACILITY_RPC  <br/> |Para los códigos de estado devueltos por llamadas a procedimiento remoto.  <br/> |
|FACILITY_STORAGE  <br/> |Para los códigos de estado devueltos desde llamadas a [métodos IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) [o IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas con el almacenamiento estructurado. Los códigos de estado con valores de código (16 bits inferiores) en el intervalo de códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.  <br/> |
   
El campo de código es un número único que se asigna para representar el error o la advertencia.
  

