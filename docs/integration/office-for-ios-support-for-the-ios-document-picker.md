---
title: Compatibilidad de Office para iOS con el Selector de documentos de iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office para iOS se integra con el Selector de documentos de iOS mediante la extensión Document Provider, que permite a Office abrir archivos almacenados por otro proveedor de documentos.
ms.openlocfilehash: 101e3cc248f994fe449a74c6c37f788fad8beed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816021"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Compatibilidad de Office para iOS con el Selector de documentos de iOS

Office para iOS se integra con el Selector de documentos de iOS mediante la extensión Document Provider, que permite a Office abrir archivos almacenados por otro proveedor de documentos.
  
Las versiones de iOS de Apple a partir de la versión iOS 8.0 incluyen [compatibilidad con extensiones de aplicación](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Puede usar estas extensiones para ampliar la funcionalidad de la aplicación en otras aplicaciones o contextos en el dispositivo del usuario. Para integrar Office para iOS con el Selector de documentos de iOS, se usa la [extensión Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).
  
La extensión Document Provider admite cuatro operaciones:
  
- Importar
    
- Exportar
    
- Abrir
    
- Mover
    
Office para iOS se integra con la operación abrir. Cuando crea una extensión Document Provider, los usuarios pueden usar el Selector de documentos para abrir y editar documentos directamente en Office sin crear una copia duplicada del archivo.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>Obtenga más información sobre las extensiones de aplicación y el Selector de documentos
<a name="bk_addresources"> </a>

- [Extensiones de aplicación](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Guía de programación del Selector de documentos](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Guía de programación de Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

