---
title: Compatibilidad de Office para iOS con el Selector de documentos de iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office para iOS se integra con el Selector de documentos de iOS mediante la extensión Document Provider, que permite a Office abrir archivos almacenados por otro proveedor de documentos.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410668"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="febb3-103">Compatibilidad de Office para iOS con el Selector de documentos de iOS</span><span class="sxs-lookup"><span data-stu-id="febb3-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="febb3-104">Office para iOS se integra con el Selector de documentos de iOS mediante la extensión Document Provider, que permite a Office abrir archivos almacenados por otro proveedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="febb3-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="febb3-p101">Las versiones de iOS de Apple a partir de la versión iOS 8.0 incluyen [compatibilidad con extensiones de aplicación](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Puede usar estas extensiones para ampliar la funcionalidad de la aplicación en otras aplicaciones o contextos en el dispositivo del usuario. Para integrar Office para iOS con el Selector de documentos de iOS, se usa la [extensión Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span><span class="sxs-lookup"><span data-stu-id="febb3-p101">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device. To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="febb3-108">La extensión Document Provider admite cuatro operaciones:</span><span class="sxs-lookup"><span data-stu-id="febb3-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="febb3-109">Importar</span><span class="sxs-lookup"><span data-stu-id="febb3-109">Import</span></span>
    
- <span data-ttu-id="febb3-110">Exportar</span><span class="sxs-lookup"><span data-stu-id="febb3-110">Export</span></span>
    
- <span data-ttu-id="febb3-111">Abrir</span><span class="sxs-lookup"><span data-stu-id="febb3-111">Open</span></span>
    
- <span data-ttu-id="febb3-112">Mover</span><span class="sxs-lookup"><span data-stu-id="febb3-112">Move</span></span>
    
<span data-ttu-id="febb3-p102">Office para iOS se integra con la operación abrir. Cuando crea una extensión Document Provider, los usuarios pueden usar el Selector de documentos para abrir y editar documentos directamente en Office sin crear una copia duplicada del archivo.</span><span class="sxs-lookup"><span data-stu-id="febb3-p102">Office for iOS integrates with the open operation. When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="febb3-115">Obtenga más información sobre las extensiones de aplicación y el Selector de documentos</span><span class="sxs-lookup"><span data-stu-id="febb3-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="febb3-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="febb3-116"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="febb3-117">Extensiones de aplicación</span><span class="sxs-lookup"><span data-stu-id="febb3-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="febb3-118">Guía de programación del Selector de documentos</span><span class="sxs-lookup"><span data-stu-id="febb3-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="febb3-119">Guía de programación de Document Provider</span><span class="sxs-lookup"><span data-stu-id="febb3-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

