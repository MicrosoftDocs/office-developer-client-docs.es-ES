---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407700"
---
# <a name="showoptions"></a>ShowOptions

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Muestra un cuadro de diálogo modal para recopilar información del usuario. Este punto de entrada se llama  cuando un  usuario hace clic en el botón Opciones situado junto  al cuadro Tipo de clúster del conector de clúster seleccionado en el cuadro de diálogo Opciones de **Excel** (en la categoría Avanzadas de la sección **Fórmulas).** Los conectores de clúster son responsables de implementar su propia interfaz de diálogo de opciones y de almacenar los datos relacionados en el Registro o en otro lugar. Las opciones son internas al conector de clúster. Excel no los tiene en cuenta. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parámetros

_hWndParent_
  
> Identificador de la ventana de Excel.
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si se mostró el cuadro de diálogo; **xlHpcRetCallFailed** si no se mostró. 
  
## <a name="remarks"></a>Comentarios

Los conectores de clúster pueden usar este cuadro de diálogo para obtener información, como el servidor de clúster que se va a usar, del usuario.
  
## <a name="see-also"></a>Consulte también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

