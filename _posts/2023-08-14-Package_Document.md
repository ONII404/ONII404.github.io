---
title: Package Document (content.opf)
author: ONII
date: 2023-08-14
category: Jekyll
layout: post
---

## Elemento `package`

Información que el elemento puede encapsular.

><dl>
>   <dt>NOMBRE</dt>
>    <dd>package</dd>
> <dt>USO</dt>
>  <dd>Obligatorio</dd>
> <dt>ATRIBUTOS</dt>
>  <dd>version [obligatorio]</dd>
>  <dd>unique-identifier [obligatorio]</dd>
>  <dd>prefix [opcional]</dd>
>  <dd>xml:lang [opcional]</dd>
>  <dd>id [opcional]</dd>
>  <dd>dir [opcional]</dd>
> <dt>HIJOS CONTENIDOS</dt>
>    <dd class="ddNote">Orden requerido:</dd>
>  <dd>metadata [solo 1]</dd>
>  <dd>manifest [solo 1]</dd>
>  <dd>spine [solo 1]</dd>
>  <dd>collection [0 o más]</dd>
></dl>
>
{: .block-doc }

El `Package Document` o `content.opf` es un documento [XML](https://www.w3.org/TR/xml/) que consiste en una serie de elementos que encapsulan información de diversos aspectos del ePub.
Unos de lo que encontraremos son:

- Metadata: — incluye o referencia información sobre el ePub.
- Manifest: — incluye e identifica todos los ítems del ePub.
- Spine: — lista ordenada de los ítems `XHTML` del ePub.

Ejemplo xx:

~~~XML
<?xml version="1.0" encoding="utf-8"?>
<package ...>
    <metadata ...>
        <!-- elemetos del metadata -->
    </metadata>
 
    <manifest>
        <!-- elemetos del manifest -->
    </manifest>
 
    <spine>
        <!-- elemetos del Spine -->
    </spine>
</package>
~~~

El elemento `package` es el elemento raíz del `Package Document` y debe contener los siguientes atributos:

~~~XML
<?xml version="1.0" encoding="utf-8"?>
    <package version="3.0" 
    unique-identifier="BookId" 
    prefix="onix: http://www.editeur.org/ONIX/book/codelists/current.html#" 
    xml:lang="es" 
    xmlns="http://www.idpf.org/2007/opf">

    <!-- elemeto metadata -->
    <!-- elemeto manifest -->
    <!-- elemeto Spine -->
</package>
~~~

# Sección de Metadata

## El elemento `metadata`

Información que el elemento puede encapsular.

><dl>
>   <dt>NOMBRE</dt>
>    <dd>metadata</dd>
> <dt>USO*</dt>
>  <dd>Obligatorio (*primer hijo de package*)</dd>
> <dt>ATRIBUTOS</dt>
>  <dd>no requiere</dd>
> <dt>HIJOS CONTENIDOS</dt>
>    <dd class="ddNote">Orden requerido:</dd>
>  <dd>dc:identifier [1 o más]</dd>
>  <dd>dc:title [1 o más]</dd>
>  <dd>dc:language [1 o más]</dd>
>  <dd>meta [1 o más]</dd>
>  <dd>link [0 o más]</dd>
></dl>
>
{: .block-doc }

Las funciones principales del elemento `metadata` del `Package Document` son:

- Proporcionar información para que los sistemas de lectura utilicen para catalogar e identificar un ePub.
- proporcionar acceso a todos los metadatos para controlar el diseño y visualización del contenido.

El elemento `metadata` debe contener de forma mínima los \[[dcterms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)\] dejando el resto de la metadata como *OPCIONAL*
Los \[[dcterms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)\] son:

## Elementos Dublin Core Requeridos

### El elemento `dc:identifier`

El elemento `dc:identifier` puede contener un identificador UUID, DOI o ISBN.

><dl>
>   <dt>NOMBRE</dt>
>       <dd>dc:identifier</dd>
>   <dt>USO</dt>
>       <dd>Obligatorio (Hijo de metadata)</dd>
>   <dt>ATRIBUTOS</dt>
>       <dd>id [obligatorio]</dd>
>   <dt>CONTENIDO</dt>
>       <dd>Texto</dd>
></dl>
{: .block-doc }

### El elemento `dc:title`

Información que el elemento puede encapsular.

><dl>
>   <dt>NOMBRE</dt>
>       <dd>dc:title</dd>
>   <dt>USO</dt>
>       <dd>Obligatorio (Hijo de metadata)</dd>
>   <dt>ATRIBUTOS</dt>
>       <dd>dir [Opcional]</dd>
>       <dd>id [Opcional]</dd>
>       <dd>xml:lang [Opcional]</dd>
>   <dt>CONTENIDO</dt>
>       <dd>Texto</dd>
></dl>
{: .block-doc }

### El elemento `dc:language`

Información que el elemento puede encapsular.

><dl>
>   <dt>NOMBRE</dt>
>       <dd>dc:language</dd>
>   <dt>USO</dt>
>       <dd>Obligatorio (Hijo de metadata)</dd>
>   <dt>ATRIBUTOS</dt>
>       <dd>id [Opcional]</dd>
>   <dt>CONTENIDO</dt>
>       <dd>Texto</dd>
></dl>
{: .block-doc }

## Elementos Dublin Core Opcionales
