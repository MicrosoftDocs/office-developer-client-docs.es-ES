---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815699"
---
# <a name="showoptions"></a>ShowOptions

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Muestra un cuadro de diálogo modal para recopilar información del usuario. En este punto de entrada se llama cuando un usuario hace clic en el botón de **Opciones** situada junto al cuadro **tipo de clúster** para el conector de clúster seleccionado en el cuadro de diálogo **Opciones de Excel** (en la categoría **Avanzadas** , en la sección **fórmulas** ). Conectores de clúster son responsables para implementar su propia interfaz de cuadro de diálogo Opciones y para almacenar los datos relacionados en el registro o en otro lugar. Las opciones son internas para el conector de clúster. Excel no es consciente de ellos. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parámetros

_hWndParent_
  
> Identificador de la ventana de Excel.
    
## <a name="return-value"></a>Valor devuelto

**xlHpcRetSuccess** si se muestra el cuadro de diálogo; **xlHpcRetCallFailed** si no se muestra. 
  
## <a name="remarks"></a>Comentarios

Conectores de clúster pueden usar este cuadro de diálogo para obtener información, por ejemplo, qué servidor de clúster se usa, desde el usuario.
  
## <a name="see-also"></a>Vea también

- [Funciones de conectores clúster de Excel](excel-cluster-connector-functions.md)

