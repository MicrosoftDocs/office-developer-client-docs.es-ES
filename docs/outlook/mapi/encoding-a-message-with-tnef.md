---
title: Codificar un mensaje con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336704"
---
# <a name="encoding-a-message-with-tnef"></a>Codificar un mensaje con TNEF

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se envía un mensaje, el proveedor de transporte puede crear un archivo que se usa para contener el mensaje durante la transmisión. A continuación, se ajusta una interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) alrededor del archivo. A continuación, el proveedor de transporte usa métodos [ITnef](itnefiunknown.md) para escribir las propiedades del mensaje en la secuencia en un formato etiquetado que permite que los proveedores de transporte de recepción puedan descodificar fácilmente las propiedades. 
  
**Para representar un mensaje completo en un solo archivo**
  
1. Para obtener un objeto TNEF, pase un [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y un mensaje a la [función OpenTnefStreamEx.](opentnefstreamex.md) 
    
2. Para obtener una lista de todas las propiedades definidas para el mensaje, llame al [método IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
3. Use [métodos IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades admitidas por el sistema de mensajería. En el momento adecuado, escriba esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería. 
    
4. Llama [a ITnef::AddProps](itnef-addprops.md) para codificar las propiedades restantes, incluidos todos los datos adjuntos. 
    
5. Llame al [método ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de agregar todas las propiedades solicitadas. 
    
6. Llame al [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para obtener el texto del mensaje etiquetado. Este texto etiquetado se escribe en el sistema de mensajería mediante métodos de la interfaz OLE [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
7. Llame al [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) para liberar el **objeto ITnef.** 
    
**Para procesar un mensaje TNEF entrante**
  
1. Obtener un objeto de mensaje MAPI de la cola MAPI y escribir propiedades de encabezado de mensaje en el nuevo mensaje MAPI.
    
2. Cree e inicialice [un objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para que contenga los datos TNEF del mensaje entrante. 
    
3. Pase el mensaje MAPI y el [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a la [función OpenTnefStreamEx.](opentnefstreamex.md) 
    
4. Descodificar la información de los datos de TNEF llamando al [método ITnef::ExtractProps.](itnef-extractprops.md) 
    
   > [!NOTE]
   > Cualquier cosa descodificada por **ExtractProps** sobrescribirá las propiedades descodificadas del sobre del mensaje entrante. Es decir, las propiedades TNEF extraídas sobrescribirán las propiedades existentes en un mensaje. 
  
5. Procese el texto del mensaje etiquetado llamando a [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) y analice el texto para recuperar posiciones de datos adjuntos. 
    
6. Guarde el mensaje llamando a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
7. Libere el objeto TNEF llamando al [método IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) 
    

