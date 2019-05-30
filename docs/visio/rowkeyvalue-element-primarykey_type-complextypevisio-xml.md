---
title: Elemento RowKeyValue (complexType PrimaryKey_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica el valor de una clave principal para una fila individual de un objeto Recordset.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538133"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>Elemento RowKeyValue (complexType PrimaryKey_Type) (XML de Visio)

Especifica el valor de una clave principal para una fila individual de un objeto Recordset.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[ClavePrincipal](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Especifica una clave principal de un objeto Recordset.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Pseudocolumna  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Un valor único que identifica una fila de un objeto Recordset.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Valor  <br/> |xsd: String  <br/> |necesario  <br/> |El valor de la clave principal de esta fila del objeto Recordset.  <br/> |Valores del tipo xsd: String.  <br/> |
   

