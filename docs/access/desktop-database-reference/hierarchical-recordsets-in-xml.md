---
title: Conjuntos de registros jerárquicos en XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0aafaa1f7f49d34d647ec0f733e68de21cb5369
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709036"
---
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="0c21a-102">Conjuntos de registros jerárquicos en XML</span><span class="sxs-lookup"><span data-stu-id="0c21a-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="0c21a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c21a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="0c21a-104">Conjuntos de registros jerárquicos en XML</span><span class="sxs-lookup"><span data-stu-id="0c21a-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="0c21a-p101">ADO permite la persistencia de objetos **Recordset** jerárquicos en XML. Con objetos **Recordset** jerárquicos, el valor de un campo en el **conjunto de registros** principal es otro **conjunto de registros**. Estos campos se representan como elementos secundarios en la secuencia XML y no como atributos. En el ejemplo siguiente, se muestra este caso:</span><span class="sxs-lookup"><span data-stu-id="0c21a-p101">ADO allows persistence of hierarchical **Recordset** objects into XML. With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**. Such fields are represented as child elements in the XML stream rather than an attribute. The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="0c21a-109">A continuación, se muestra el formato XML del **conjunto de registros** conservado:</span><span class="sxs-lookup"><span data-stu-id="0c21a-109">The following is the XML format of the persisted **Recordset**:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

<span data-ttu-id="0c21a-p102">El orden exacto de las columnas del **conjunto de registros** principal no es obvio cuando persiste de esta forma. Cualquier campo del **conjunto de registros** principal puede contener un conjunto de registros secundario. El proveedor de persistencia primero conserva todas las columnas escalares como atributos y luego todas las "columnas" **Recordset** secundarias como elementos secundarios de la fila principal. La posición ordinal del campo en el **conjunto de registros** principal se puede obtener consultando la definición de esquema del **conjunto de registros**. Cada campo tiene una propiedad de OLE DB, **rs:number**, definida en el espacio de nombres de esquema del **conjunto de registros** que contiene el número ordinal correspondiente a ese campo.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p102">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner. Any field in the parent may contain a child **Recordset**. The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row. The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**. Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="0c21a-p103">Los nombres de todos los campos del **conjunto de registros** secundario se concatenan con el nombre del campo del **conjunto de registros** principal que contiene este secundario. De este modo, se garantiza que no hay conflictos de nombres en los casos en los que tanto el **conjunto de registros** principal como el secundario contienen un campo que se obtiene de dos tablas diferentes pero con nombre singular.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p103">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child. This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="0c21a-117">Cuando se guardan **conjunto de registros** jerárquicos en XML, se deben tener en cuenta las restricciones siguientes en ADO:</span><span class="sxs-lookup"><span data-stu-id="0c21a-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="0c21a-118">Un **conjunto de registros** jerárquico con actualizaciones pendientes no puede persistir en XML.</span><span class="sxs-lookup"><span data-stu-id="0c21a-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="0c21a-119">Un **conjunto de registros** jerárquico creado con un comando Shape parametrizado no puede persistir (en formato XML o ADTG).</span><span class="sxs-lookup"><span data-stu-id="0c21a-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="0c21a-p104">Actualmente, ADO guarda la relación entre los **conjuntos de registros** principal y secundario como un objeto binario grande (BLOB). Todavía no se han definido etiquetas XML en el espacio de nombres de esquema de conjunto de filas para describir esta relación.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p104">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB). XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="0c21a-p105">Cuando se guarda un **conjunto de registros** jerárquico, todos los **conjuntos de registros** secundarios se guardan con él. Si el **conjunto de registros** activo es secundario de otro **conjunto de registros**, el principal no se guarda. Todos los **conjuntos de registros** secundarios que componen el subárbol del **conjunto de registros** activo sí se guardan.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p105">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it. If the current **Recordset** is a child of another **Recordset**, its parent is not saved. All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="0c21a-125">Cuando se vuelve a abrir un **conjunto de registros** jerárquico desde su formato XML persistente, se deben tener en cuenta las limitaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="0c21a-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="0c21a-p106">Si el registro secundario contiene registros a los que no corresponden registros principales, estas filas no se escriben en la representación XML del **conjunto de registros** jerárquico. Por lo tanto, estas filas se perderán cuando el **conjunto de registros** se vuelva a abrir desde su ubicación persistente.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p106">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**. Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="0c21a-p107">Si un registro secundario tiene referencias a más de un registro principal, cuando se abra el **conjunto de registros**, el **conjunto de registros** secundario podrá contener registros duplicados. No obstante, estos duplicados sólo estarán visibles si el usuario trabaja directamente con el conjunto de filas secundario subyacente. Si se utiliza un capítulo para desplazarse por el **conjunto de registros** secundario (que es la única forma de desplazarse por ADO), los duplicados no estarán visibles.</span><span class="sxs-lookup"><span data-stu-id="0c21a-p107">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records. However, these duplicates will only be visible if the user works directly with the underlying child rowset. If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

